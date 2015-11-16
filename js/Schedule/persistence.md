---
title: State persistence
description: How to persist schedule properties
platform: js
control: schedule
documentation: ug
keywords: persist, state persist, persistence, state persistence 
---
## Persistence

State persistence allows the Scheduler to retain the current model value in the browser cookies for state maintenance. This action is handled through the property **[enablePersistence](http://help.syncfusion.com/js/api/ejschedule#members:enablepersistence "")** which is set to false by default.

When it is set to **true**, some of the Schedule control model values will be retained even after refreshing the page which are listed below.

<table>
<tr>
<td>
currentView<br/><br/></td><td>
timeMode<br/><br/></td></tr>
<tr>
<td>
firstDayOfWeek<br/><br/></td><td>
dateFormat<br/><br/></td></tr>
<tr>
<td>
isDST<br/><br/></td><td>
timeZone<br/><br/></td></tr>
<tr>
<td>
Timescale<br/><br/></td><td>
startHour<br/><br/></td></tr>
<tr>
<td>
endHour<br/><br/></td><td>
workHours<br/><br/></td></tr>
<tr>
<td>
Height<br/><br/></td><td>
Width<br/><br/></td></tr>
<tr>
<td>
cellHeight<br/><br/></td><td>
cellWidth<br/><br/></td></tr>
<tr>
<td>
currentDate<br/><br/></td><td>
minDate<br/><br/></td></tr>
<tr>
<td>
maxDate<br/><br/></td><td>
renderDates<br/><br/></td></tr>
<tr>
<td>
Orientation<br/><br/></td><td>
Views<br/><br/></td></tr>
<tr>
<td>
workWeek<br/><br/></td><td>
agendaViewSettings.daysInAgenda<br/><br/></td></tr>
<tr>
<td>
enableLoadOnDemand<br/><br/></td><td>
showLocationField<br/><br/></td></tr>
<tr>
<td>
showAllDayRow<br/><br/></td><td>
isResponsive<br/><br/></td></tr>
<tr>
<td>
enableRecurrenceValidation<br/><br/></td><td>
<br/><br/></td></tr>
</table>
The Schedule properties that are not retained while maintaining state persistence are included within the **ignoreOnPersist** list, which makes it not to persist by default.

