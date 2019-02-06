---
layout: post
title: Custom Actions | ReportViewer | JavaScript | Syncfusion
description: Add custom button and action to email a report using JavaScript Report Viewer.
platform: js
control: ReportViewer
documentation: ug
---

# Custom Actions (Email a report)
Add user defined buttons and invoke custom actions using Report Viewer property options. In this section, we will create custom action to email the rendered report to users.

## Add email button

1.Create email button option in toolbar, using the [`customToolBarItems`](../api/ejreportviewer#members:toolbarSettings-customtoolbaritems) property with values such as index, cssClass name, tooltip, click event to fire when click the button.
2.Access the Report Viewer model and create json array for sending to Web API server. You can use the following codes for creating the event with custom action.  

{% highlight javascript %}
    <script type="text/javascript">
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: {
                        click: 'emailReport',
                        customToolBarItems: [{
                            itemType: ej.ReportViewer.InputElement.Default,
                            groupIndex: 3,
                            index: 2,
                            cssClass: "e-icon e-mail e-reportviewer-icon",
                            tooltip: {
                                header: 'E-Mail',
                                content: 'Send rendered report as mail attachment',
                            },

                            click: 'emailReport'
                        }]
                    }
                });
        });
        function emailReport(args) {
            var proxy = $('#container').data('ejReportViewer');
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
    </script>
{% endhighlight %}

N> In the above code sample, report is exported to PDF and sent to users, using smptClient.

## Create custom email action

1.Create a new action method `SendEmail` in Web API service.
2.Export the report to required type using ReportHelper.GetReport to send report stream as attachment.
3.The following code sample exports the report to stream and send it as attachment to a specified mail address. Here in the code, used SmtpClient to send the report as email attachment.

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

4.Build and run the application, to view the Report Viewer with custom toolbar option.

![Report Viewer with custom email option in toolbar](images/report-service/email-report.png)