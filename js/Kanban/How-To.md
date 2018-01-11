---
layout: post
title: How to section in Kanban widget for Essential JS? 
description: How to achieve specific requirements in Kanban widget for Essential JS
platform: js
control: Kanban
documentation: ug
keywords: how to 
api: /api/js/ejkanban
---

# How To?

## Dynamically change swimlane key

Swimlane key categorization of Kanban control can be changed dynamically using set model method.  We have created an external drop down list that contains the Kanban swimlane keys and based on the selected drop down value, [swimlaneKey](https://help.syncfusion.com/api/js/ejkanban#members:fields-swimlanekey) value is assigned using set model.  Please find the below code.

{% highlight html %}

        <select id="dropdown">
	         <option value="Assignee">Assignee</option>
			 <option value="Status">Status</option>
	    </select>
        <div id="Kanban"></div>

    <script type="text/javascript">
        $(function () {
		 var kanbanData = [
                 { Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Type: "Story", Priority: "Low", Tags: "Analyze,Customer", Estimate: 3.5, Assignee: "Andrew Fuller", ImgUrl:"/images/kanban/1.png", RankId: 1 },
				 { Id: 2, Status: "InProgress", Summary: "Improve application performance", Type: "Improvement", Priority: "Normal", Tags: "Improvement", Estimate: 6, Assignee: "Andrew Fuller", ImgUrl: "/images/kanban/2.png", RankId: 1 },
				 { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Type: "Others", Priority: "Critical", Tags: "Meeting", Estimate: 5.5, Assignee: "Janet", ImgUrl: "/images/kanban/3.png", RankId: 2 },
				 { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Type: "Bug", Priority: "Release Breaker", Tags: "IE", Estimate: 2.5, Assignee: "Janet", ImgUrl: "/images/kanban/3.png", RankId: 2 },
				 { Id: 5, Status: "Close", Summary: "Fix the issues reported by the customer.", Type: "Bug", Priority: "Low", Tags: "Customer", Estimate: "3.5", Assignee: "Andrew Fuller", ImgUrl: "/images/kanban/5.png", RankId: 1 }
		      ];
            var data = ej.DataManager(kanbanData);
            $("#Kanban").ejKanban(
                {
                    dataSource: data,
                    columns: [
                        { headerText: "Backlog", key: "Open" },
                        { headerText: "In Progress", key: "InProgress" },
                        { headerText: "Done", key: "Close" }
                    ],                                                           			
                    keyField: "Status",
					fields: {
					    content: "Summary",
					    primaryKey: "Id"
					},
					allowSelection: false
                });
		    $('#dropdown').ejDropDownList({watermarkText: "Change Assignee", change: "change"});
        });
		// Swimlane key is changed based on dropdown value.
		function change(args){
		    $("#Kanban").ejKanban("option", {"fields": { swimlaneKey: args.selectedValue } });
        }
    </script>

{% endhighlight %} 

![](how-to_images/how_to_img1.png)