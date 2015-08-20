---
layout: post
title: ejSchedule
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Schedule control.










$(element).ejSchedule<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();         
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.min.js


* module:jquery.globalize.min.js


* module:jsrender.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.schedule.js


* module:ej.scroller.js


* module:ej.radiobutton.js


* module:ej.editor.js


* module:ej.dropdownlist.js


* module:ej.autocomplete.js


* module:ej.menu.js


* module:ej.dialog.js


* module:ej.button.js


* module:ej.checkbox.js


* module:ej.datepicker.js


* module:ej.timepicker.js


* module:ej.navigationdrawer.js




## Members








### allowDragDrop<span class="type-signature type boolean">boolean</span>
{:#members:allowdragdrop}








Enables or disables the appointment drag and drop behavior of schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ 
    allowDragDrop: true,
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }   
       });
</script>{% endhighlight %}







### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}








Enables or disables the keyboard interaction of schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ allowKeyboardNavigation: true});
</script>{% endhighlight %}







### appointmentSettings<span class="type-signature type object">Object</span>
{:#members:appointmentsettings}








This property is used to bind the appointmentSettings data fields to the schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.allDay<span class="type-signature type string">string</span>
{:#members:appointmentsettings-allday}








Bind string value to allday field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.categorize<span class="type-signature type string">string</span>
{:#members:appointmentsettings-categorize}








Bind string value to categorize field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay",
              categorize: "Categorize"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.dataSource<span class="type-signature type object">object</span>
{:#members:appointmentsettings-datasource}








Render the appointments within the Schedule control based on the specified dataSource.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.description<span class="type-signature type string">string</span>
{:#members:appointmentsettings-description}








Bind string value to description field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { description: "Description",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",               
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.endTime<span class="type-signature type string">string</span>
{:#members:appointmentsettings-endtime}








Bind string value to endTime field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { endTime: "EndTime",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.endTimeZone<span class="type-signature type string">string</span>
{:#members:appointmentsettings-endtimezone}








Bind string value to endTimeZone field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { endTimeZone: "EndTimeZone",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.id<span class="type-signature type string">string</span>
{:#members:appointmentsettings-id}








Bind string value to id field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { id: "Id",
              dataSource: window.Default, //collection of object from dataSource.                *               
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.location<span class="type-signature type string">string</span>
{:#members:appointmentsettings-location}








Bind string value to location field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay",
              categorize: "Categorize",
              location:"Location",
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.priority<span class="type-signature type string">string</span>
{:#members:appointmentsettings-priority}








Bind string value to priority field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay",
              categorize: "Categorize",
              location:"Location",
              priority:"Priority"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.query<span class="type-signature type object">object</span>
{:#members:appointmentsettings-query}








Query the data records from the table for schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.recurrence<span class="type-signature type string">string</span>
{:#members:appointmentsettings-recurrence}








Bind string value to recurrence field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { recurrence: "Recurrence",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.recurrenceRule<span class="type-signature type string">string</span>
{:#members:appointmentsettings-recurrencerule}








Bind string value to recurrenceRule field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { recurrenceRule: "RecurrenceRule",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.resourceFields<span class="type-signature type string">string</span>
{:#members:appointmentsettings-resourcefields}








Binds the resource related fields to the schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ 
     resources: [
     {
       field: "ownerId",
       title: "Owner",
       name: "Owners", allowMultiple: true,
       resourceSettings: { dataSource: [
       { text: "Andrew", id: 1, groupId: 1, color: "#f8a398" },
       { text: "Cruise", id: 3, groupId: 2, color: "#56ca85" },
       { text: "Jerry", id: 5, groupId: 1, color: "#51a0ed" }],    
       text: "text", id: "id", groupId: "groupId", color: "color" }
     }],    
     appointmentSettings: { dataSource: window.ResourcesData, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay",
              resourceFields: "ownerId"
            } 
     });  
</script>{% endhighlight %}







### appointmentSettings.startTime<span class="type-signature type string">string</span>
{:#members:appointmentsettings-starttime}








Bind string value to startTime field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { startTime: "StartTime",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",               
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.startTimeZone<span class="type-signature type string">string</span>
{:#members:appointmentsettings-starttimezone}








Bind string value to startTimeZone field of schedule.





Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { startTimeZone: "StartTimeZone",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",               
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.subject<span class="type-signature type string">string</span>
{:#members:appointmentsettings-subject}








Bind string value to subject field of schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { subject: "Subject",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentSettings.tableName<span class="type-signature type string">string</span>
{:#members:appointmentsettings-tablename}








Specify the tablename to retrive the data for schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { tableName:"tablename",
              dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                                      
   });
</script>{% endhighlight %}







### appointmentTemplateId<span class="type-signature type string">string</span>
{:#members:appointmenttemplateid}








Specifies an element&rsquo;s id which can be used for appointment template rendering.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ appointmentTemplateId: "#templatename"});
</script>{% endhighlight %}







### businessEndHour<span class="type-signature type number">number</span>
{:#members:businessendhour}








Apply the business end hour of the schedule.




Default Value:
{:.param}






* 18








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ highlightBusinessHours : true, businessEndHour: 16});
</script>{% endhighlight %}







### businessStartHour<span class="type-signature type number">number</span>
{:#members:businessstarthour}








Apply the business start hour of the schedule.




Default Value:
{:.param}






* 9








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ highlightBusinessHours : true, businessStartHour: 7});
</script>  {% endhighlight %}







### categorizeSettings<span class="type-signature type object">Object</span>
{:#members:categorizesettings}








This property is used to bind the Categorize items of schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  categorizeSettings: {
      enable: true,
      }
   });
</script>{% endhighlight %}







### categorizeSettings.allowMultiple<span class="type-signature type boolean">boolean</span>
{:#members:categorizesettings-allowmultiple}








allowMultiple option enables/disables the multiple selection of categories for the appointments.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ categorizeSettings:{allowMultiple: false}});
</script>{% endhighlight %}







### categorizeSettings.color<span class="type-signature type string">string</span>
{:#members:categorizesettings-color}








Bind string value to color field of categorize.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  categorizeSettings:{
   enable:true,
   allowMultiple:false,
     dataSource:[
    { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },
    { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },
    { text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },
    { text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },
    { text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },
    { text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }                
    ],            
     text: "text",
     id:"id",
     color:"color",
     fontColor:"fontColor"
      }
     }                                      
   });
</script>{% endhighlight %}







### categorizeSettings.dataSource<span class="type-signature type object">object</span>
{:#members:categorizesettings-datasource}








Defines the Categorize data collection for the schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ categorizeSettings:{enable: true,allowMultiple:false,
 dataSource:[
 { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },
 { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },
 { text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },
 { text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },
 { text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },
 { text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }                
 ],
  });
</script>{% endhighlight %}







### categorizeSettings.enable<span class="type-signature type boolean">boolean</span>
{:#members:categorizesettings-enable}








Enables or disables the Categorize option for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ categorizeSettings:{enable: false}});
</script>{% endhighlight %}







### categorizeSettings.fontColor<span class="type-signature type string">string</span>
{:#members:categorizesettings-fontcolor}








Bind string value to fontColor field of categorize.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  categorizeSettings:{
   enable:true,
   allowMultiple:false,
     dataSource:[
    { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },
    { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },
    { text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },
    { text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },
    { text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },
    { text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }                
    ],            
     text: "text",
     id:"id",
     color:"color",
     fontColor:"fontColor"
      }
     }                                      
   });
</script>{% endhighlight %}







### categorizeSettings.id<span class="type-signature type string">string</span>
{:#members:categorizesettings-id}








Bind string value to id field of categorize.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  categorizeSettings:{
   enable:true,
   allowMultiple:false,
     dataSource:[
    { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },
    { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },
    { text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },
    { text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },
    { text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },
    { text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }                
    ],            
     text: "text",
     id:"id",
     color:"color",
     fontColor:"fontColor"
      }
     }                                      
   });
</script>{% endhighlight %}







### categorizeSettings.text<span class="type-signature type string">string</span>
{:#members:categorizesettings-text}








Bind string value to text field of categorize.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  categorizeSettings:{
   enable:true,
   allowMultiple:false,
     dataSource:[
    { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },
    { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },
    { text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },
    { text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },
    { text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },
    { text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }                
    ],            
     text: "text",
     id:"id",
     color:"color",
     fontColor:"fontColor"
      }
     }                                      
   });
</script>{% endhighlight %}







### cellHeight<span class="type-signature type string">string</span>
{:#members:cellheight}








Defines the Cell height of the schedule.




Default Value:
{:.param}






* "20px"








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ cellHeight: "100px"});
</script>{% endhighlight %}







### cellWidth<span class="type-signature type string">string</span>
{:#members:cellwidth}








Defines the Cell Width of the schedule.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ cellWidth: "100px"});
</script>{% endhighlight %}







### contextMenuSettings<span class="type-signature type object">Object</span>
{:#members:contextmenusettings}








This property is used to bind the contextmenu items of schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  contextMenuSettings: {
      enable: true,
      }
   });
</script>{% endhighlight %}







### contextMenuSettings.enable<span class="type-signature type boolean">boolean</span>
{:#members:contextmenusettings-enable}








Enables or disables the context menu option for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ contextMenuSettings:{enable: true}});
</script>{% endhighlight %}







### contextMenuSettings.menuItems<span class="type-signature type object">object</span>
{:#members:contextmenusettings-menuitems}








Context menu collection for appointment and cells of schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ contextMenuSettings:{enable: true,
      menuItems:{appointment: [
       { id: "open", text: "Open Appointment" },
       { id: "delete", text: "Delete Appointment" }
   ],
   cells: [
       { id: "new", text: "New Appointment" },
       { id: "recurrence", text: "New Recurring Appointment" },
       { id: "today", text: "Today" },
       { id: "gotodate", text: "Go to date" },
       { id: "settings", text: "Settings" },
       { id: "view", text: "View", parentId: "settings" },
       { id: "timemode", text: "TimeMode", parentId: "settings" },
       { id: "view_Day", text: "Day", parentId: "view" },
       { id: "view_Week", text: "Week", parentId: "view" },
       { id: "view_Workweek", text: "Workweek", parentId: "view" },
       { id: "view_Month", text: "Month", parentId: "view" },
       { id: "timemode_Hour12", text: "12 Hours", parentId: "timemode" },
       { id: "timemode_Hour24", text: "24 Hours", parentId: "timemode" },
       { id: "businesshours", text: "Business Hours", parentId: "settings" }
   ]}
  }
  });
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class for schedule to achieve the custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ cssClass: "gradient-lime"});
</script>{% endhighlight %}







### currentDate<span class="type-signature type date">date</span>
{:#members:currentdate}








Apply the current date to the schedule.




Default Value:
{:.param}






* new Date()








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ currentDate: new Date()});
</script>{% endhighlight %}







### currentView<span class="type-signature type enum">enum</span>
{:#members:currentview}








Specifies the current view of the schedule; See <a href="global.html#CurrentView">CurrentView</a>




Default Value:
{:.param}






* ej.Schedule.CurrentView.Week








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
        $("#Schedule").ejSchedule({ currentView: ej.Schedule.CurrentView.Day});
</script>{% endhighlight %}







### dateFormat<span class="type-signature type string">String</span>
{:#members:dateformat}








Defines the date format of the schedule.




Default Value:
{:.param}






* "MM/dd/yyyy"








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
        $("#Schedule").ejSchedule({  dateFormat: "dd/MM/yyyy" });
</script>{% endhighlight %}







### enableAppointmentNavigation<span class="type-signature type boolean">boolean</span>
{:#members:enableappointmentnavigation}








Enables or disables the previous/next appointment navigation of schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ 
      enableAppointmentNavigation: true,
      currentDate:new Date(2014,1,1),
      appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }
      });
</script>{% endhighlight %}







### enableAppointmentResize<span class="type-signature type boolean">boolean</span>
{:#members:enableappointmentresize}








Enables or disables the appointment resize behavior of schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ 
    enableAppointmentResize: true,
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }   
      });
</script>{% endhighlight %}







### enableLoadOnDemand<span class="type-signature type boolean">boolean</span>
{:#members:enableloadondemand}








Enables/disables the load on demand option for schedule appointment data.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ enableLoadOnDemand: false});
</script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}








Saves the current model value to the browser cookies for state maintanence. When we refresh the page, the Schedule control values will be retained.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ enablePersistence: true});
</script>{% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Enables or disables the resize behavior of schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ enableResize: false});
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Enables or disables the rtl direction for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ enableRTL: true});
</script>{% endhighlight %}







### endHour<span class="type-signature type number">number</span>
{:#members:endhour}








Apply the end hour to the work area of schedule.




Default Value:
{:.param}






* 24








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ endHour: 18});
</script>{% endhighlight %}







### group<span class="type-signature type object">Object</span>
{:#members:group}








Groups the specified resources in the schedule control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ 
      group: {
          resources: ["Rooms","Owners"]
      },    
      resources: [{
       field: "ownerId",
       title: "Owner",
       name: "Owners", allowMultiple: true,
       resourceSettings: { dataSource: [
       { text: "Room1", id: 1, color: "#f8a398" }], 
       text: "text", id: "id",  color: "color" }
     },
      {
          field: "roomId",
          title: "Room",
          name: "Rooms", allowMultiple: false,
          resourceSettings: { dataSource: [
          { text: "Andrew", id: 1, groupId: 1, color: "#f8a398" },
          { text: "Jerry", id: 2, groupId: 1, color: "#56ca85"}],
            text: "text", id: "id", groupId: "groupId", color: "color"
          }
       }],
      appointmentSettings: {
          dataSource: window.ResourcesData,
          id: "Id",
          subject: "Subject",
          startTime: "StartTime",
          endTime: "EndTime",
          allDay: "AllDay",
          recurrence: "Recurrence",
          recurrenceRule: "RecurrenceRule",
          resourceFields: "roomId,ownerId"
      } 
   });  
</script>{% endhighlight %}







### height<span class="type-signature type string">string</span>
{:#members:height}








Defines the height of the schedule.




Default Value:
{:.param}






* "800px"








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ height: "700px"});
</script>{% endhighlight %}







### highlightBusinessHours<span class="type-signature type boolean">boolean</span>
{:#members:highlightbusinesshours}








Enable or disable the business-hour highlighting behavior for schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ highlightBusinessHours: false});
</script>{% endhighlight %}







### isDST<span class="type-signature type boolean">boolean</span>
{:#members:isdst}








Enable or disable the Daylight Saving Time (DST) behavior for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ isDST: true});
</script>{% endhighlight %}







### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members:isresponsive}








Enables or disables the adaptive of schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ isResponsive: true});
</script>{% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Defines the locale for schedule.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ locale: "en-US"});
</script>{% endhighlight %}







### maxDate<span class="type-signature type date">date</span>
{:#members:maxdate}








Defines the Maximum date of the schedule.




Default Value:
{:.param}






* maxDate: new Date(2099, 12, 31)








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ maxDate: new Date("20/11/2014")});
</script>{% endhighlight %}







### minDate<span class="type-signature type date">date</span>
{:#members:mindate}








Defines the Minimum date of the schedule.




Default Value:
{:.param}






* new Date(1900, 01, 01)








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ minDate: new Date("10/11/2014")});
</script>{% endhighlight %}







### orientation<span class="type-signature type enum">enum</span>
{:#members:orientation}








Defines the orientation type of the schedule; Renders the schedule either in vertical or horizontal mode as specified through this property.




Default Value:
{:.param}






* ej.Schedule.Orientation.Vertical








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
        $("#Schedule").ejSchedule({ orientation: ej.Schedule.Orientation.Horizontal});
</script>{% endhighlight %}







### prioritySettings<span class="type-signature type object">Object</span>
{:#members:prioritysettings}








prioritySettings is an object collection that holds the priority related information. 




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ prioritySettings:{enable: true}});
</script>{% endhighlight %}







### prioritySettings.dataSource<span class="type-signature type object">object</span>
{:#members:prioritysettings-datasource}








Defines the Priority data collection for the schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ prioritySettings:{enable: true,dataSource:[
 { text: "None", id: 1, value: "none" },
 { text: "High", id: 2, value: "high" },
 { text: "Medium", id: 3, value: "medium" },
 { text: "Low", id: 4, value: "low" }               
 ],          
     text: "text",
     id:"id",
     value:"value"
     }
     });
        {% endhighlight %}











### prioritySettings.enable<span class="type-signature type boolean">boolean</span>
{:#members:prioritysettings-enable}








Enables or disables the Priority option for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}

<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ prioritySettings:{enable: false}});
</script>{% endhighlight %}







### prioritySettings.id<span class="type-signature type string">string</span>
{:#members:prioritysettings-id}








Bind string/int value to id field of priority.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   prioritySettings:{
   enable:true,
   template:"",
 dataSource:[
 { text: "None", id: 1, value: "none" },
 { text: "High", id: 2, value: "high" },
 { text: "Medium", id: 3, value: "medium" },
 { text: "Low", id: 4, value: "low" }               
 ],          
     text: "text",
     id:"id",
     value:"value"
      }                                       
   });
</script>
{% endhighlight %}








### prioritySettings.template<span class="type-signature type boolean">boolean</span>
{:#members:prioritysettings-template}








template option to display the priority icons for the appointments.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ prioritySettings:{template: "<div class='${value}'></div>",  // To display the Priority option in the appointment window while passing custom datasource we need to mention the template like this
        }
        });
        {% endhighlight %}











### prioritySettings.text<span class="type-signature type string">string</span>
{:#members:prioritysettings-text}








Bind string value to text field of priority.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   prioritySettings:{
   enable:true,
   template:"",
 dataSource:[
 { text: "None", id: 1, value: "none" },
 { text: "High", id: 2, value: "high" },
 { text: "Medium", id: 3, value: "medium" },
 { text: "Low", id: 4, value: "low" }               
 ],          
     text: "text",
     id:"id",
     value:"value"
      }                                           
   });
</script>
{% endhighlight %}








### prioritySettings.value<span class="type-signature type string">string</span>
{:#members:prioritysettings-value}








Bind string value to value field of priority.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
      
<div id="Schedule"></div>  
<script>
$("#Schedule").ejSchedule({
   prioritySettings:{
   enable:true,
   template:"",
 dataSource:[
 { text: "None", id: 1, value: "none" },
 { text: "High", id: 2, value: "high" },
 { text: "Medium", id: 3, value: "medium" },
 { text: "Low", id: 4, value: "low" }               
 ],          
     text: "text",
     id:"id",
     value:"value"
      }                                           
   });
</script>
{% endhighlight %}







### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}








Enable or disable the interaction with appointments in schedule.




Default Value:
{:.param}






* false








Example
{:.example}



{% highlight html %}

<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ readOnly: false});
</script>{% endhighlight %}







### reminderSettings<span class="type-signature type object">Object</span>
{:#members:remindersettings}








This property is used to set the reminder options of schedule.




Default Value:
{:.param}






* {enable: false, alertBefore: 5}








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  reminderSettings: {
      enable: true,
      }
   });
</script>{% endhighlight %}







### reminderSettings.alertBefore<span class="type-signature type number">number</span>
{:#members:remindersettings-alertbefore}








Set the alert timing in reminder settings option of schedule.




Default Value:
{:.param}






* 5








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ reminderSettings:{enable: true, alertBefore:6}});
</script>{% endhighlight %}







### reminderSettings.enable<span class="type-signature type boolean">boolean</span>
{:#members:remindersettings-enable}








Enables or disables the reminder settings option for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ reminderSettings:{enable: true}});
</script>{% endhighlight %}







### renderDates<span class="type-signature type object">Object</span>
{:#members:renderdates}








Defines the specific start and end dates to be rendered in the schedule control. To render such user-specified custom dates in the schedule control, it is necessary to set the currentView property of the schedule to customview.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
        $("#Schedule").ejSchedule({ 
          views: ["Day", "Week", "WorkWeek", "Month", "CustomView"], 
          currentView: ej.Schedule.CurrentView.CustomView,
          renderDates: {
              start: new Date(2014, 11, 7),
              end: new Date(2014, 12, 10)
          }
  });
</script>{% endhighlight %}







### resourceHeaderTemplateId<span class="type-signature type string">string</span>
{:#members:resourceheadertemplateid}








Specifies an element&rsquo;s id which can be used for resource header template rendering.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ resourceHeaderTemplateId: "#resTemplate"});
</script>{% endhighlight %}







### resources<span class="type-signature type object">Object</span>
{:#members:resources}








Binds the resource collection to the schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ 
     resources: [
     {
       field: "ownerId",
       title: "Owner",
       name: "Owners", allowMultiple: true,
       resourceSettings: { dataSource: [
       { text: "Andrew", id: 1, groupId: 1, color: "#f8a398" },
       { text: "Cruise", id: 3, groupId: 2, color: "#56ca85" },
       { text: "Jerry", id: 5, groupId: 1, color: "#51a0ed" }],    
       text: "text", id: "id", groupId: "groupId", color: "color" }
     }],    
     appointmentSettings: { dataSource: window.ResourcesData, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay",
              resourceFields: "ownerId"
            } 
     });  
</script>{% endhighlight %}







### showAllDayRow<span class="type-signature type boolean">boolean</span>
{:#members:showalldayrow}








Show/hide the allday row cells of the schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ showAllDayRow: true});
</script>{% endhighlight %}







### showCurrentTimeIndicator<span class="type-signature type boolean">boolean</span>
{:#members:showcurrenttimeindicator}








Enables or disables the display of current time indicator on the schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ showCurrentTimeIndicator: true});
</script>{% endhighlight %}







### showHeaderBar<span class="type-signature type boolean">boolean</span>
{:#members:showheaderbar}








Enable or disable the header bar of the schedule control.





Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ showHeaderBar: false});
</script>{% endhighlight %}








### showLocationField<span class="type-signature type boolean">boolean</span>
{:#members:showlocationfield}








Enable or disable the location field display behavior for schedule.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ showLocationField: true});
</script>{% endhighlight %}







### showQuickWindow<span class="type-signature type boolean">boolean</span>
{:#members:showquickwindow}








Enable or disable the quick window open behavior for schedule.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ showQuickWindow: false});
</script>{% endhighlight %}







### showTimeScale<span class="type-signature type boolean">boolean</span>
{:#members:showtimescale}








Enable or disable the time scale behavior for schedule.





Default Value:
{:.param}






* true








Example
{:.example}



{% highlight html %}
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ showTimeScale: false});
</script>{% endhighlight %}







### startHour<span class="type-signature type number">number</span>
{:#members:starthour}








Apply the start hour to the work area of schedule.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ startHour: 9});
</script>{% endhighlight %}







### timeMode<span class="type-signature type enum">enum</span>
{:#members:timemode}








Defines the time mode of the schedule; To know more on timemodes of the schedule. See <a href="global.html#TimeMode">TimeMode</a>




Default Value:
{:.param}






* ej.Schedule.TimeMode.Hour12








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
        $("#Schedule").ejSchedule({ timeMode: ej.Schedule.TimeMode.Hour24});
</script>{% endhighlight %}







### timeZone<span class="type-signature type string">string</span>
{:#members:timezone}








Defines the timeZone of the schedule.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ timeZone: "UTC +2:00"});
</script>{% endhighlight %}







### timezoneCollection<span class="type-signature type object">Object</span>
{:#members:timezonecollection}








This property is used to bind the timezoneCollection items of schedule.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  timezoneCollection: {
      }
   });
</script>{% endhighlight %}







### timezoneCollection.dataSource<span class="type-signature type object">object</span>
{:#members:timezonecollection-datasource}








Binds the timezone collection values specified in the dataSource to the Schedule control.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ timezoneCollection:{
        dataSource: [
       { text: "UTC -12:00", id:"1", value: "UTC -12:00" },
       { text: "UTC -11:00", id:"2", value: "UTC -11:00" },
       { text: "UTC -10:00", id:"3", value: "UTC -10:00" },
       { text: "UTC -09:00", id:"4", value: "UTC -09:00" },
       { text: "UTC -08:00", id:"5", value: "UTC -08:00" },
       { text: "UTC -07:00", id:"6", value: "UTC -07:00" }
          ]
          }
  });
</script>{% endhighlight %}







### timezoneCollection.id<span class="type-signature type string">string</span>
{:#members:timezonecollection-id}








Binds the id field name to the id property of the timezoneCollection dataSource.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  timezoneCollection:{
        dataSource: [
       { text: "UTC -12:00", id:"1", value: "UTC -12:00" },
       { text: "UTC -11:00", id:"2", value: "UTC -11:00" },
       { text: "UTC -10:00", id:"3", value: "UTC -10:00" },
       { text: "UTC -09:00", id:"4", value: "UTC -09:00" },
       { text: "UTC -08:00", id:"5", value: "UTC -08:00" },
       { text: "UTC -07:00", id:"6", value: "UTC -07:00" }
          ],           
     text: "text",
     id:"id",
     value:"value"
      }                                      
   });
</script>{% endhighlight %}







### timezoneCollection.text<span class="type-signature type string">string</span>
{:#members:timezonecollection-text}








Binds the text field name to the text property of the timezoneCollection dataSource.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  timezoneCollection:{
        dataSource: [
       { text: "UTC -12:00", id:"1", value: "UTC -12:00" },
       { text: "UTC -11:00", id:"2", value: "UTC -11:00" },
       { text: "UTC -10:00", id:"3", value: "UTC -10:00" },
       { text: "UTC -09:00", id:"4", value: "UTC -09:00" },
       { text: "UTC -08:00", id:"5", value: "UTC -08:00" },
       { text: "UTC -07:00", id:"6", value: "UTC -07:00" }
          ],           
     text: "text",
     id:"id",
     value:"value"
      }                                      
   });
</script>{% endhighlight %}







### timezoneCollection.value<span class="type-signature type string">string</span>
{:#members:timezonecollection-value}








Binds the value field name to the value property of the timezoneCollection dataSource.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
       
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
  timezoneCollection:{
        dataSource: [
       { text: "UTC -12:00", id:"1", value: "UTC -12:00" },
       { text: "UTC -11:00", id:"2", value: "UTC -11:00" },
       { text: "UTC -10:00", id:"3", value: "UTC -10:00" },
       { text: "UTC -09:00", id:"4", value: "UTC -09:00" },
       { text: "UTC -08:00", id:"5", value: "UTC -08:00" },
       { text: "UTC -07:00", id:"6", value: "UTC -07:00" }
          ],           
     text: "text",
     id:"id",
     value:"value"
      }                                      
   });
</script>{% endhighlight %}







### views<span class="type-signature type array.string">Array.string</span>
{:#members:views}








Defines the collection of views to be displayed in the schedule control.




Default Value:
{:.param}






* [ "Day" , "Week" , "WorkWeek" , "Month" ]








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
        $("#Schedule").ejSchedule({ views: ["Day","Month"], currentView:"day"});
</script>{% endhighlight %}







### width<span class="type-signature type string">string</span>
{:#members:width}








Defines the width of the schedule.




Default Value:
{:.param}






* "800px"








Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
        $("#Schedule").ejSchedule({ width: "700px"});
</script>{% endhighlight %}





## Methods








### deleteAppointment<span class="signature">()</span>
{:#methods:deleteappointment}








It is used to delete the appointment. The id is based on the argument passed along with this method

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">id value of the appointment</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.deleteAppointment(105); //Appointments id number.
</script>{% endhighlight %}







### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the schedule widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.destroy(); // destroy the schedule
</script>{% endhighlight %}







### exportSchedule<span class="signature">()</span>
{:#methods:exportschedule}








It used to Export the appointments from the schedule control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to refer the controller action name to redirect. (For MVC)</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.serverEvent{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to refer the server event name.(For ASP)</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to pass the id of an appointment, in case if a single appointment needs to be exported. Otherwise, it takes the null value.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.exportSchedule("ActionName","ExportToICS", null); // To Export all the Appointments
schObj.exportSchedule("ActionName","ExportToICS", 101); // To Export a single appointment with an id "101"
</script>{% endhighlight %}







### filterAppointments<span class="signature">()</span>
{:#methods:filterappointments}








It used search the appointments from appointment list of schedule control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.filterConditions{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">filterConditions value of the filter collections for appointments.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
var filter=[{
   field: "Subject",
   operator: "contains",
   value: "gold",
   predicate: "or"
}];
var appointments=schObj.filterAppointments(filter); // Gets the appointments list of schedule control
</script>{% endhighlight %}







### getAppointments<span class="signature">()</span>
{:#methods:getappointments}








It is used to get the appointment list of schedule control.





Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
var appointments=schObj.getAppointments(); // Gets the appointments list of schedule control
</script>{% endhighlight %}







### print<span class="signature">()</span>
{:#methods:print}








It is used to print the schedule.





Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.print();
</script>{% endhighlight %}







### refreshScroller<span class="signature">()</span>
{:#methods:refreshscroller}








It used to Refresh Scroller while using schedule control in some other controls.





Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.refreshScroller(); // To refresh scroller while using schedule control in some other control
</script>{% endhighlight %}







### saveAppointment<span class="signature">()</span>
{:#methods:saveappointment}








It is used to save the appointment. The appointment obj is based on the argument passed along with this method.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.obj{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">obj of the appointment</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.saveAppointment(obj); //obj contains collection of appointment. 
</script>{% endhighlight %}







### searchAppointments<span class="signature">()</span>
{:#methods:searchappointments}








It used search the appointments from appointment list of schedule control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.searchString{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">searchString value of the search word in the appointments.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.fields{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fields value of which feilds need search.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.filterOperator{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">filterOperator value of the search operation need to done.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.ignoreCase{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">ignoreCase value of the case.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
var appointments=schObj.searchAppointments("gold"); // Gets the appointments list of schedule control
</script>{% endhighlight %}





## Events








### actionBegin
{:#events:actionbegin}








Triggers before the action begin of the schedule.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when view change action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Date{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentView{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current view value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the click.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when date navigate action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the click.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when date change by calendar action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the click.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment save action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the save appointment value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment edit action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the edit appointment value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment delete action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
id{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the id of delete appointment.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment drag action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the appointment we drag.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment resize action starts:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the appointment we resize.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   actionBegin: function (args) {}
});
</script>{% endhighlight %}







### actionComplete
{:#events:actioncomplete}








Triggers after the action completion of the schedule.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when view change action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about viewchange action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when date navigate action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about the date navigate action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when date change by calendar action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about calendar navigation action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment save action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about appointment saved value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment edit action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about appointment edited value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment delete action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about appointment deleted action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment dragging action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the appointment data we dropped.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters when appointment resizing action completed:
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the element we resized.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
requestType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   actionComplete: function (args) {}
});
</script>{% endhighlight %}







### appointmentClick
{:#events:appointmentclick}








Triggers after the appointment is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentClick event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the clicked appointment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },   
   appointmentClick: function (args) {}
});
</script>{% endhighlight %}







### appointmentDeleted
{:#events:appointmentdeleted}








Triggers after the appointment is deleted.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentDeleted event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the deleted appintment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   appointmentDeleted: function (args) {}
});
</script>{% endhighlight %}







### appointmentEdited
{:#events:appointmentedited}








Triggers after the appointment is edited.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentEdited event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the edited appintment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   appointmentEdited: function (args) {}
});
</script>{% endhighlight %}








### appointmentHover
{:#events:appointmenthover}








Triggers after the appointment is hovered.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentHover event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the hovered appointment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },   
   appointmentHover: function (args) {}
});
</script>{% endhighlight %}







### appointmentSaved
{:#events:appointmentsaved}








Triggers after the appointment is saved.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentSaved event using appointment window.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the saved appintment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentSaved event using quick window.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the saved appintment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   appointmentSaved: function (args) {}
});
</script>{% endhighlight %}







### appointmentWindowOpen
{:#events:appointmentwindowopen}








Triggers before the appointment window is opened.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of appointmentWindowOpen event while select detail option from quick window.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.endTime{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the end time of the double clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.originalEventType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action name which triggers window open.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.startTime{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the start time of the double clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the double clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of edit appointmentWindowOpen event while select edit appointment/edit series option.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the edit appointment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.edit{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the edit occurrence option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   appointmentWindowOpen: function (args) {}
});
</script>{% endhighlight %}







### beforeContextMenuOpen
{:#events:beforecontextmenuopen}








Triggers before the context menu open up.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of beforeContextMenuOpen event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.events{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the object of before open menu target.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   beforeContextMenuOpen: function (args) {}
});
</script>{% endhighlight %}







### cellClick
{:#events:cellclick}








Triggers after the cell is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of cellClick event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.endTime{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the end time of the clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.startTime{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the start time of the clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   cellClick: function (args) {}
});
</script>{% endhighlight %}







### cellDoubleClick
{:#events:celldoubleclick}








Triggers after the cell is clicked twice.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of cellDoubleClick event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.endTime{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the end time of the double clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.startTime{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the start time of the double clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the double clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   cellDoubleClick: function (args) {}
});
</script>{% endhighlight %}







### cellHover
{:#events:cellhover}








Triggers after the cell is hovered.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of cellHover event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cellIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the index of the hovered cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date of the hovered cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the clicked cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   cellHover: function (args) {}
});
</script>{% endhighlight %}







### drag
{:#events:drag}








Triggers while the appointment is being dragged over the workcells.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of dragOver event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the drag over appointment.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   drag: function (args) {}
});
</script>{% endhighlight %}







### dragStart
{:#events:dragstart}








Triggers when the appointment dragging begins.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of dargStart event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the dragging appointment.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   dragStart: function (args) {}
});
</script>{% endhighlight %}







### dragStop
{:#events:dragstop}








Triggers when the appointment is dropped.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of dragDrop event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dropped appointment object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   dragStop: function (args) {}
});
</script>{% endhighlight %}







### menuItemClick
{:#events:menuitemclick}








Triggers after the context menu is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of menuItemClick event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.events{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the object of menu item event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   menuItemClick: function (args) {}
});
</script>{% endhighlight %}







### navigation
{:#events:navigation}








Triggers after the Schedule view or date is navigated.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of schedule view navigation event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.Date{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentView{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current view value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevView{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the previous view value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of previous/next date navigation event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the new date of the schedule.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous date of the schedule.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the navigation event while change the date using calendar in schedule.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the new date of the schedule.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDate{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous date of the schedule.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the action.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   navigation: function (args) {}
});
</script>{% endhighlight %}







### reminder
{:#events:reminder}








Triggers when the reminder is raised for an appointment.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.reminderAppointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the appointment object for which the reminder is raised.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   reminder: function (args) {}
});
</script>{% endhighlight %}







### resize
{:#events:resize}








Triggers while resizing the appointment.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of resizing event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the resize element value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   resize: function (args) {}
});
</script>{% endhighlight %}







### resizeStart
{:#events:resizestart}








Triggers when the appointment resizing begins.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of resizeStart event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the resize element value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   resizeStart: function (args) {}
});
</script>{% endhighlight %}







### resizeStop
{:#events:resizestop}








Triggers when appointment resizing is stopped.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of resizeStop event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.appointment{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the resized appointment value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the resized appointment.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { dataSource: window.Default, //collection of object from dataSource.
              id: "Id",
              subject: "Subject",
              description: "Description",
              startTime: "StartTime",
              endTime: "EndTime",
              recurrence: "Recurrence",
              recurrenceRule: "RecurrenceRule",
              allDay: "AllDay"
            },
   resizeStop: function (args) {}
});
</script>{% endhighlight %}




