---
layout: post
title: ejSchedule
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html Schedule control.










#### $(element).ejSchedule<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$('#Schedule').ejSchedule();         
&lt;/script&gt;</code>
</pre>






### Requires




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




### Members








#### allowDragDrop<span class="type-signature type boolean">boolean</span>








Enables or disables the appointment drag and drop behavior of schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>








Enables or disables the keyboard interaction of schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ allowKeyboardNavigation: true});
&lt;/script&gt;</code>
</pre>






#### appointmentSettings<span class="type-signature type object">Object</span>








This property is used to bind the appointmentSettings data fields to the schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.allDay<span class="type-signature type string">string</span>








Bind string value to allday field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.categorize<span class="type-signature type string">string</span>








Bind string value to categorize field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.dataSource<span class="type-signature type object">object</span>








Render the appointments within the Schedule control based on the specified dataSource.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.description<span class="type-signature type string">string</span>








Bind string value to description field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.endTime<span class="type-signature type string">string</span>








Bind string value to endTime field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.id<span class="type-signature type string">string</span>








Bind string value to id field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.location<span class="type-signature type string">string</span>








Bind string value to location field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.priority<span class="type-signature type string">string</span>








Bind string value to priority field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.query<span class="type-signature type object">object</span>








Query the data records from the table for schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.recurrence<span class="type-signature type string">string</span>








Bind string value to recurrence field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.recurrenceRule<span class="type-signature type string">string</span>








Bind string value to recurrenceRule field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.resourceFields<span class="type-signature type string">string</span>








Binds the resource related fields to the schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.startTime<span class="type-signature type string">string</span>








Bind string value to startTime field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.subject<span class="type-signature type string">string</span>








Bind string value to subject field of schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSettings.tableName<span class="type-signature type string">string</span>








Specify the tablename to retrive the data for schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentTemplateId<span class="type-signature type string">string</span>








Specifies an element&rsquo;s id which can be used for appointment template rendering.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ appointmentTemplateId: "#templatename"});
&lt;/script&gt;</code>
</pre>






#### businessEndHour<span class="type-signature type number">number</span>








Apply the business end hour of the schedule.




Default Value:






* 18








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ highlightBusinessHours : true, businessEndHour: 16});
&lt;/script&gt;</code>
</pre>






#### businessStartHour<span class="type-signature type number">number</span>








Apply the business start hour of the schedule.




Default Value:






* 9








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ highlightBusinessHours : true, businessStartHour: 7});
&lt;/script&gt;  </code>
</pre>






#### categorizeSettings<span class="type-signature type object">Object</span>








This property is used to bind the Categorize items of schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
  categorizeSettings: {
      enable: true,
      }
   });
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.allowMultiple<span class="type-signature type boolean">boolean</span>








allowMultiple option enables/disables the multiple selection of categories for the appointments.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ categorizeSettings:{allowMultiple: false}});
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.color<span class="type-signature type string">string</span>








Bind string value to color field of categorize.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.dataSource<span class="type-signature type object">object</span>








Defines the Categorize data collection for the schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.enable<span class="type-signature type boolean">boolean</span>








Enables or disables the Categorize option for schedule.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ categorizeSettings:{enable: false}});
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.fontColor<span class="type-signature type string">string</span>








Bind string value to fontColor field of categorize.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.id<span class="type-signature type string">string</span>








Bind string value to id field of categorize.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### categorizeSettings.text<span class="type-signature type string">string</span>








Bind string value to text field of categorize.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### cellHeight<span class="type-signature type string">string</span>








Defines the Cell height of the schedule.




Default Value:






* "20px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ cellHeight: "100px"});
&lt;/script&gt;</code>
</pre>






#### cellWidth<span class="type-signature type string">string</span>








Defines the Cell Width of the schedule.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ cellWidth: "100px"});
&lt;/script&gt;</code>
</pre>






#### contextMenuSettings<span class="type-signature type object">Object</span>








This property is used to bind the contextmenu items of schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
  contextMenuSettings: {
      enable: true,
      }
   });
&lt;/script&gt;</code>
</pre>






#### contextMenuSettings.enable<span class="type-signature type boolean">boolean</span>








Enables or disables the context menu option for schedule.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ contextMenuSettings:{enable: true}});
&lt;/script&gt;</code>
</pre>






#### contextMenuSettings.menuItems<span class="type-signature type object">object</span>








Context menu collection for appointment and cells of schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Specify the CSS class for schedule to achieve the custom theme.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ cssClass: "gradient-lime"});
&lt;/script&gt;</code>
</pre>






#### currentDate<span class="type-signature type date">date</span>








Apply the current date to the schedule.




Default Value:






* new Date()








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ currentDate: new Date()});
&lt;/script&gt;</code>
</pre>






#### currentView<span class="type-signature type enum">enum</span>








Specifies the current view of the schedule; See <a href="global.html#CurrentView">CurrentView</a>




Default Value:






* ej.Schedule.CurrentView.Week








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#Schedule").ejSchedule({ currentView: ej.Schedule.CurrentView.Day});
&lt;/script&gt;</code>
</pre>






#### dateFormat<span class="type-signature type string">String</span>








Defines the date format of the schedule.




Default Value:






* "MM/dd/yyyy"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#Schedule").ejSchedule({  dateFormat: "dd/MM/yyyy" });
&lt;/script&gt;</code>
</pre>






#### enableAppointmentNavigation<span class="type-signature type boolean">boolean</span>








Enables or disables the previous/next appointment navigation of schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### enableAppointmentResize<span class="type-signature type boolean">boolean</span>








Enables or disables the appointment resize behavior of schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### enableLoadOnDemand<span class="type-signature type boolean">boolean</span>








Enables/disables the load on demand option for schedule appointment data.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ enableLoadOnDemand: false});
&lt;/script&gt;</code>
</pre>






#### enablePersistence<span class="type-signature type boolean">boolean</span>








Saves the current model value to the browser cookies for state maintanence. When we refresh the page, the Schedule control values will be retained.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ enablePersistence: true});
&lt;/script&gt;</code>
</pre>






#### enableResize<span class="type-signature type boolean">boolean</span>








Enables or disables the resize behavior of schedule.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ enableResize: false});
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Enables or disables the rtl direction for schedule.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ enableRTL: true});
&lt;/script&gt;</code>
</pre>






#### endHour<span class="type-signature type number">number</span>








Apply the end hour to the work area of schedule.




Default Value:






* 24








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ endHour: 18});
&lt;/script&gt;</code>
</pre>






#### group<span class="type-signature type object">Object</span>








Groups the specified resources in the schedule control.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### height<span class="type-signature type string">string</span>








Defines the height of the schedule.




Default Value:






* "800px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ height: "700px"});
&lt;/script&gt;</code>
</pre>






#### highlightBusinessHours<span class="type-signature type boolean">boolean</span>








Enable or disable the business-hour highlighting behavior for schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ highlightBusinessHours: false});
&lt;/script&gt;</code>
</pre>






#### isResponsive<span class="type-signature type boolean">boolean</span>








Enables or disables the adaptive of schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ isResponsive: true});
&lt;/script&gt;</code>
</pre>






#### locale<span class="type-signature type string">string</span>








Defines the locale for schedule.




Default Value:






* "en-US"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ locale: "en-US"});
&lt;/script&gt;</code>
</pre>






#### maxDate<span class="type-signature type date">date</span>








Defines the Maximum date of the schedule.




Default Value:






* maxDate: new Date(2099, 12, 31)








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ maxDate: new Date("20/11/2014")});
&lt;/script&gt;</code>
</pre>






#### minDate<span class="type-signature type date">date</span>








Defines the Minimum date of the schedule.




Default Value:






* new Date(1900, 01, 01)








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ minDate: new Date("10/11/2014")});
&lt;/script&gt;</code>
</pre>






#### orientation<span class="type-signature type enum">enum</span>








Defines the orientation type of the schedule; Renders the schedule either in vertical or horizontal mode as specified through this property.




Default Value:






* ej.Schedule.Orientation.Vertical








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#Schedule").ejSchedule({ orientation: ej.Schedule.Orientation.Horizontal});
&lt;/script&gt;</code>
</pre>






#### prioritySettings.dataSource<span class="type-signature type object">object</span>








Defines the Priority data collection for the schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ prioritySettings:{enable: true,template:"</code>
</pre>










#### <code>prioritySettings.enable<span class="type-signature type boolean">boolean</span></code>








<code>Enables or disables the Priority option for schedule.</code>




<code>Default Value:</code>






* <code>false</code>








##### <code>Example</code>

<pre class="prettyprint">
<code><code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ prioritySettings:{enable: false}});
&lt;/script&gt;</code></code>
</pre>






#### prioritySettings.id<span class="type-signature type string">string</span>








Bind string/int value to id field of priority.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   prioritySettings:{
   enable:true,
   template:"</code>
</pre>



<pre>
",
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
     }                                      
   });
&lt;/script&gt;
</pre>






#### <code>prioritySettings.template<span class="type-signature type boolean">boolean</span></code>








<code>template option to display the priority icons for the appointments.</code>




<code>Default Value:</code>






* <code>null</code>








##### <code>Example</code>

<pre class="prettyprint">
<code><code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ prioritySettings:{template: "</code></code>
</pre>










#### <code>prioritySettings.text<span class="type-signature type string">string</span></code>








<code>Bind string value to text field of priority.</code>




<code>Default Value:</code>






* <code>null</code>








##### <code>Example</code>

<pre class="prettyprint">
<code><code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   prioritySettings:{
   enable:true,
   template:"</code></code>
</pre>



<pre>
",
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
     }                                      
   });
&lt;/script&gt;
</pre>






#### <code>prioritySettings.value<span class="type-signature type string">string</span></code>








<code>Bind string value to value field of priority.</code>




<code>Default Value:</code>






* <code>null</code>








##### <code>Example</code>

<pre class="prettyprint">
<code><code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   prioritySettings:{
   enable:true,
   template:"</code></code>
</pre>



<pre>
",
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
     }                                      
   });
&lt;/script&gt;
</pre>






#### <code>readOnly<span class="type-signature type boolean">boolean</span></code>








<code>Enable or disable the interaction with appointments in schedule.</code>




<code>Default Value:</code>






* <code>false</code>








##### <code>Example</code>

<pre class="prettyprint">
<code><code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ readOnly: false});
&lt;/script&gt;</code></code>
</pre>






#### reminderSettings<span class="type-signature type object">Object</span>








This property is used to set the reminder options of schedule.




Default Value:






* {enable: false, alertBefore: 5}








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
  reminderSettings: {
      enable: true,
      }
   });
&lt;/script&gt;</code>
</pre>






#### reminderSettings.alertBefore<span class="type-signature type number">number</span>








Set the alert timing in reminder settings option of schedule.




Default Value:






* 5








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ reminderSettings:{enable: true, alertBefore:6}});
&lt;/script&gt;</code>
</pre>






#### reminderSettings.enable<span class="type-signature type boolean">boolean</span>








Enables or disables the reminder settings option for schedule.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ reminderSettings:{enable: true}});
&lt;/script&gt;</code>
</pre>






#### renderDates<span class="type-signature type object">Object</span>








Defines the specific start and end dates to be rendered in the schedule control. To render such user-specified custom dates in the schedule control, it is necessary to set the currentView property of the schedule to customview.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#Schedule").ejSchedule({ 
          views: ["Day", "Week", "WorkWeek", "Month", "CustomView"], 
          currentView: ej.Schedule.CurrentView.CustomView,
          renderDates: {
              start: new Date(2014, 11, 7),
              end: new Date(2014, 12, 10)
          }
  });
&lt;/script&gt;</code>
</pre>






#### resourceHeaderTemplateId<span class="type-signature type string">string</span>








Specifies an element&rsquo;s id which can be used for resource header template rendering.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ resourceHeaderTemplateId: "#resTemplate"});
&lt;/script&gt;</code>
</pre>






#### resources<span class="type-signature type object">Object</span>








Binds the resource collection to the schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### showAllDayRow<span class="type-signature type boolean">boolean</span>








Show/hide the allday row cells of the schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ showAllDayRow: true});
&lt;/script&gt;</code>
</pre>






#### showCurrentTimeIndicator<span class="type-signature type boolean">boolean</span>








Enables or disables the display of current time indicator on the schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ showCurrentTimeIndicator: true});
&lt;/script&gt;</code>
</pre>






#### showLocationField<span class="type-signature type boolean">boolean</span>








Enable or disable the location field display behavior for schedule.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ showLocationField: true});
&lt;/script&gt;</code>
</pre>






#### showQuickWindow<span class="type-signature type boolean">boolean</span>








Enable or disable the quick window open behavior for schedule.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ showQuickWindow: false});
&lt;/script&gt;</code>
</pre>






#### startHour<span class="type-signature type number">number</span>








Apply the start hour to the work area of schedule.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ startHour: 9});
&lt;/script&gt;</code>
</pre>






#### timeMode<span class="type-signature type enum">enum</span>








Defines the time mode of the schedule; To know more on timemodes of the schedule. See <a href="global.html#TimeMode">TimeMode</a>




Default Value:






* ej.Schedule.TimeMode.Hour12








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#Schedule").ejSchedule({ timeMode: ej.Schedule.TimeMode.Hour24});
&lt;/script&gt;</code>
</pre>






#### timeZone<span class="type-signature type string">string</span>








Defines the timeZone of the schedule.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ timeZone: "UTC +2:00"});
&lt;/script&gt;</code>
</pre>






#### timezoneCollection<span class="type-signature type object">Object</span>








This property is used to bind the timezoneCollection items of schedule.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
  timezoneCollection: {
      }
   });
&lt;/script&gt;</code>
</pre>






#### timezoneCollection.dataSource<span class="type-signature type object">object</span>








Binds the timezone collection values specified in the dataSource to the Schedule control.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### timezoneCollection.id<span class="type-signature type string">string</span>








Binds the id field name to the id property of the timezoneCollection dataSource.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### timezoneCollection.text<span class="type-signature type string">string</span>








Binds the text field name to the text property of the timezoneCollection dataSource.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### timezoneCollection.value<span class="type-signature type string">string</span>








Binds the value field name to the value property of the timezoneCollection dataSource.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code>       
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### views<span class="type-signature type array.string">Array.string</span>








Defines the collection of views to be displayed in the schedule control.




Default Value:






* [ "Day" , "Week" , "WorkWeek" , "Month" ]








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#Schedule").ejSchedule({ views: ["Day","Month"], currentView:"day"});
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type string">string</span>








Defines the width of the schedule.




Default Value:






* "800px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#Schedule").ejSchedule({ width: "700px"});
&lt;/script&gt;</code>
</pre>




### Methods








#### deleteAppointment<span class="signature">()</span>








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
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">id value of the appointment</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### destroy<span class="signature">()</span>








destroy the schedule widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.destroy(); // destroy the schedule
&lt;/script&gt;</code>
</pre>






#### exportSchedule<span class="signature">()</span>








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
<td class="name"><code>argument.action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to refer the controller action name to redirect. (For MVC)</td>
</tr>
<tr>
<td class="name"><code>argument.serverEvent</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to refer the server event name.(For ASP)</td>
</tr>
<tr>
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to pass the id of an appointment, in case if a single appointment needs to be exported. Otherwise, it takes the null value.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### filterAppointments<span class="signature">()</span>








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
<td class="name"><code>argument.filterConditions</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">filterConditions value of the filter collections for appointments.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### getAppointments<span class="signature">()</span>








It is used to get the appointment list of schedule control.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### print<span class="signature">()</span>








It is used to print the schedule.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### refreshScroller<span class="signature">()</span>








It used to Refresh Scroller while using schedule control in some other controls.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.refreshScroller(); // To refresh scroller while using schedule control in some other control
&lt;/script&gt;</code>
</pre>






#### saveAppointment<span class="signature">()</span>








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
<td class="name"><code>argument.obj</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">obj of the appointment</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### searchAppointments<span class="signature">()</span>








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
<td class="name"><code>argument.searchString</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">searchString value of the search word in the appointments.</td>
</tr>
<tr>
<td class="name"><code>argument.fields</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fields value of which feilds need search.</td>
</tr>
<tr>
<td class="name"><code>argument.filterOperator</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">filterOperator value of the search operation need to done.</td>
</tr>
<tr>
<td class="name"><code>argument.ignoreCase</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">ignoreCase value of the case.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>




### Events








#### actionBegin








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>Date</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date value.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentView</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current view value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the click.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentDate</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the click.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>currentDate</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the click.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the save appointment value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the edit appointment value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>id</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the id of delete appointment.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the appointment we drag.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the appointment we resize.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action begin request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   actionBegin: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### actionComplete








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about viewchange action.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about the date navigate action.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about calendar navigation action.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about appointment saved value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about appointment edited value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the data about appointment deleted action.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the appointment data we dropped.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the element we resized.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>requestType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action complete request type.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   actionComplete: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### appointmentClick








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentClick event.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the clicked appointment object.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentDeleted








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentDeleted event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the deleted appintment object.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentEdited








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentEdited event.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the edited appintment object.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### appointmentSaved








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentSaved event using appointment window.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the saved appintment object.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of appointmentSaved event using quick window.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the saved appintment object.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   appointmentSaved: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### appointmentWindowOpen








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of appointmentWindowOpen event while select detail option from quick window.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.endTime</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the end time of the double clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.originalEventType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the action name which triggers window open.</td>
</tr>
<tr>
<td class="name"><code>argument.startTime</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the start time of the double clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the double clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of edit appointmentWindowOpen event while select edit appointment/edit series option.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the edit appointment object.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.edit</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the edit occurrence option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   appointmentWindowOpen: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### beforeContextMenuOpen








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of beforeContextMenuOpen event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.events</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the object of before open menu target.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   beforeContextMenuOpen: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### cellClick








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of cellClick event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.endTime</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the end time of the clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.startTime</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the start time of the clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   cellClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### cellDoubleClick








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of cellDoubleClick event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.endTime</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the end time of the double clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.startTime</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the start time of the double clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the double clicked cell.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   cellDoubleClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### drag








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of dragOver event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the drag over appointment.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### dragStart








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of dargStart event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the dragging appointment.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### dragStop








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of dragDrop event.</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the dropped appointment object.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### menuItemClick








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of menuItemClick event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.events</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the object of menu item event.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   menuItemClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### navigation








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of schedule view navigation event.</td>
</tr>
<tr>
<td class="name"><code>argument.Date</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current date object.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.currentView</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current view value.</td>
</tr>
<tr>
<td class="name"><code>argument.prevView</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the previous view value.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the action.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of previous/next date navigation event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.currentDate</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the new date of the schedule.</td>
</tr>
<tr>
<td class="name"><code>argument.prevDate</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous date of the schedule.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the action.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the navigation event while change the date using calendar in schedule.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.currentDate</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the new date of the schedule.</td>
</tr>
<tr>
<td class="name"><code>argument.prevDate</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previous date of the schedule.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the action.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   navigation: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### reminder








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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>argument.reminderAppointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the appointment object for which the reminder is raised.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#Schedule").ejSchedule({
   reminder: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### resize








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of resizing event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the resize element value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### resizeStart








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of resizeStart event.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the resize element value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>






#### resizeStop








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
<td class="name"><code>argument.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Returns the object of resizeStop event</td>
</tr>
<tr>
<td class="name"><code>argument.appointment</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the resized appointment value.</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the schedule model.</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target of the resized appointment.</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="Schedule"&gt;&lt;/div&gt; 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>



