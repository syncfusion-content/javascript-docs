---
layout: post
title: Custom Actions | Report Viewer | JavaScript | Syncfusion
description: Add custom button and action to email a report using JavaScript Report Viewer.
platform: js
control: Report Viewer
documentation: ug
---

# Custom Actions
Add user defined buttons in the toolbar and invoke custom actions using the Report Viewer property. In this section, custom email option is created to email the rendered report to the users.

## Add email button

1.Create email button option in the toolbar using the [`customItems`](../api/ejreportviewer#members:toolbarsettings-customitems) property with the values such as `groupIndex`, `index`, `itemType`, `cssClass`, `tooltip`, `toolBarItemClick` event to fire when you click the button.
2.Access the Report Viewer model and create a JSON array for sending requests to the Web API server. You can use the following codes for creating the event with custom action.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: {
                        showToolbar: true,
                        items: ej.ReportViewer.ToolbarItems.All & ~ej.ReportViewer.ToolbarItems.Print,
                        customItems: [{
                            groupIndex: 1,
                            index: 1,
                            itemType: 'Default',
                            cssClass: "e-icon e-mail e-reportviewer-icon",
                            tooltip: {
                                header: 'E-Mail',
                                content: 'Send rendered report as mail attachment',
                                value: 'E-Mail'
                            },
                        }]

                    },
                    toolBarItemClick: 'ontoolBarItemClick',
                });
            });

            //Toolbar click event handler
            function ontoolBarItemClick(args) {
                if (args.value == "E-Mail") {
                    var proxy = $('#viewer').data('ejReportViewer');
                    var Report = proxy.model.reportPath;
                    var lastsIndex = Report.lastIndexOf("/");
                    var reportName = Report.substring(lastsIndex + 1);
                    var requrl = proxy.model.reportServiceUrl + '/SendEmail';
                    var _json = {
                        exportType: "PDF", reportViewerToken: proxy._reportViewerToken, ReportName: reportName
                    };
                    $.ajax({
                        type: "POST",
                        contentType: "application/json; charset=utf-8",
                        url: requrl,
                        data: JSON.stringify(_json),
                        dataType: "json",
                        crossDomain: true
                    })
                }
            }
        </script>
{% endhighlight %}

## Create custom email action

1.Create a new action method `SendEmail` in the Web API service.
2.Export the report to the required type using `ReportHelper.GetReport` to send report stream as an attachment.
3.The following code sample exports the report to stream and send it as an attachment to a specified mail address. In the code, `SmtpClient` is used to send the report as an email attachment.

{% highlight c# %}
        public object SendEmail(Dictionary<string, object> jsonResult)
        {
            string _token = jsonResult["reportViewerToken"].ToString();
            var stream = ReportHelper.GetReport(_token, jsonResult["exportType"].ToString());
            stream.Position = 0;
            
            if (!ComposeEmail(stream, jsonResult["reportName"].ToString()))
            {
                return "Mail not sent !!!";
            }

            return "Mail Sent !!!";
        }

        public bool ComposeEmail(Stream stream, string reportName)
        {
            try
            {
                MailMessage mail = new MailMessage();
                SmtpClient SmtpServer = new SmtpClient("smtp.gmail.com");
                mail.IsBodyHtml = true;
                mail.From = new MailAddress("xx@gmail.com");
                mail.To.Add("xx@gmail.com");
                mail.Subject = "Report Name : " + reportName;
                stream.Position = 0;

                if (stream != null)
                {
                    ContentType ct = new ContentType();
                    ct.Name = reportName + DateTime.Now.ToString() + ".pdf";
                    System.Net.Mail.Attachment attachment = new System.Net.Mail.Attachment(stream, ct);
                    mail.Attachments.Add(attachment);
                }

                SmtpServer.Port = 587;
                SmtpServer.Credentials = new System.Net.NetworkCredential("xx@gmail.com", "xx");
                SmtpServer.EnableSsl = true;
                SmtpServer.Send(mail);

                return true;
            }
            catch (Exception ex)
            {
                return ex.ToString();
            }

            return false;
        }
{% endhighlight %}

N> In the above code sample, the report is exported to PDF and sent to users using `SmptClient`.

4.Build and run the application, to view the Report Viewer with the custom toolbar option.
![Report Viewer with custom email option in toolbar](images/email-report.png)