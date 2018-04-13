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

## Update the Kanban properties dynamically after render

Properties of Kanban control can be updated dynamically by updating the model properties with new values.
For instance, if you want to change your columns property of Kanban dynamically means, this can be done by assigning newly updated columns values to existing model property [columns](https://help.syncfusion.com/api/js/ejkanban#members:columns).

{% highlight javascript %}

<script>

//  set the entire modified columns
$("#KanbanBoard").ejKanban({ columns: new_columns });

</script>

{% endhighlight %}

Code snippet to dynamically changing the column values using a button click is given below,

{% highlight javascript %}

<script>

 // button click
function onClick(e) {
        // take the Kanban instance
        var kanban_obj = $("#KanbanBoard").ejKanban("instance");

        // take the Kanban columns model using the instance
        var new_columns = kanban_obj.model.columns;

        // through the columns object change the allow drag or drop model value dynamically
        new_columns[1].allowDrag = false;
        new_columns[1].allowDrop = false;

        //set the entire modified columns
        $("#KanbanBoard").ejKanban({ columns: new_columns });
    }
</script>

{% endhighlight %}

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


## How to customize the height of the column dropping area when multiple key bound

 By default, height for the dropping clone area will be taken based on overall Kanban control height. Control height is divided into equal and assigned to each key cloned area. So, the user needs to scroll to drop to the specific cloned key area.

**Solution:**

To resolve this case, we can set the cloned area height to the visible area of Kanban instead of taking whole control height which is achieved through the code provided with the steps given.

**Step 1**:  To show all dropping area relative to the card that we are dragging, we should customize it at the sample level using the Kanban [CardDrag](https://help.syncfusion.com/api/js/ejkanban#events:carddrag) event. Create the Kanban control as shown below with cardDrag event configured.

 {% highlight html %}

   $("#Kanban").ejKanban(
                {
                    dataSource: data,
	                isResponsive:true,
                    columns: [
                        { headerText: "Backlog", key: "Open" },
                        { headerText: "In Progress", key: "InProgress,Testing,Close" },
                    ],                                                           			
                    keyField: "Status",
	                allowTitle: true,
	                fields: {
	                    content: "Summary",
					    primaryKey: "Id",
					    imageUrl: "ImgUrl"
					},
					allowSelection: false,
					cardDrag:"cardDragFun"
                });


 {% endhighlight %}
 

 **Step 2**: Add the following script to show the dynamic heights for dropping area with multiple keys within the given available space. This will also show all target column keys in the visible window space while scrolling.


 {% highlight javascript %}

   <script type="text/javascript">

    function cardDragFun(e) {

        if ($(e.dragTarget).hasClass('e-columnkey') || $(e.dragTarget).hasClass('e-rowcell')) {
            var target;
            $(e.dragTarget).hasClass('e-columnkey') ? target = $(e.dragTarget) : target = $(e.dragTarget).find('.e-columnkey');
            if (target.hasClass('e-columnkey')) {
                var scrollTop, height, scrollElem;
                var multiKeyDiv = target.parent();
                multiKeyDiv.css('vertical-align', 'top');
                if (this.model.allowScrolling && this.kanbanContent.hasClass('e-scroller')) {
                    var scrollObj = this.kanbanContent.data('ejScroller');
                    scrollTop = scrollObj.scrollTop();
                    height = this.kanbanContent.height();
                }
                else {
                    scrollElem = document.scrollingElement ? document.scrollingElement : document.documentElement
                    scrollTop = scrollElem.scrollTop === 0 ? 0 : (scrollElem.scrollTop > target.parents('.e-rowcell')[0].offsetTop ? scrollElem.scrollTop - target.parents('.e-rowcell')[0].offsetTop : target.parents('.e-rowcell')[0].offsetTop - scrollElem.scrollTop);
                    height = $(window).height() - (scrollElem.scrollTop > target.parents('.e-rowcell')[0].offsetTop ? 0 : target.parents('.e-rowcell')[0].offsetTop - scrollElem.scrollTop);
                    if ((window.innerHeight + window.scrollY) >= Math.round(document.body.offsetHeight)) {
                        height = height - ($(document).height() - (target.parents('.e-rowcell')[0].offsetHeight + target.parents('.e-rowcell')[0].offsetTop))
                    }
                }
                multiKeyDiv.height(height);
                var innerHeight = height / multiKeyDiv.children().length;
                multiKeyDiv.children().height(innerHeight);
                scrollTop > 0 ? multiKeyDiv.css('top', scrollTop) : multiKeyDiv.css('top', '');
                multiKeyDiv.find('.e-text').css('top', innerHeight / 2);
            }
        }
    }

</script>

  {% endhighlight %}


**Before Customization:**

  ![Before Customization image](how-to_images\Before_img.png)


**After Customization:**
  
  ![After Customization image](how-to_images\After_img.png)

## Customize the style of dragged Kanban card

Default styles of dragged Kanban card can be customized with CSS overriding of class **e-draggedcard**. Styles such as cards color, fonts, and any other styles can be achieved as per the user need.  Here we have modified background and font styles of card while dragging.

{% highlight html %}

<style>

    .e-kanban .e-draggedcard {  //changes the background color
        background: pink;
    }

    .e-kanban .e-draggedcard .e-text { //changes the font size
        font-size: 16px;
    }
</style>

 {% endhighlight %}

 **Before Customization:**

  ![Before Customization image](how-to_images\Before_img1.png)


**After Customization:**
  
  ![After Customization image](how-to_images\After_img1.png)