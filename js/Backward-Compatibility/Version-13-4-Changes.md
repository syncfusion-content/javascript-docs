---
layout: post
title: Backward-Compatibility - Version 13.4
description: backward compatibility - Version 13.4
platform: js
control: Introduction
documentation: ug
---

# Version 13.4 Changes

Some of the API name changes have been made to the controls to be effective from Volume 4, 2015 release. Those changes are documented by mapping the old names with appropriate new API names to enable quick upgradation of any control. To migrate from Volume 3, 2015 or from other earlier versions to this Volume 4, 2015, refer to the following API changes.

## ejSchedule

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API  Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
showTimeScale<br/><br/></td><td>
timeScale: { enable: true }<br/><br/></td><td>
Instead of showTimeScale, <br/> enable option can be used.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableAppointmentNavigation<br/><br/></td><td>
showAppointmentNavigator<br/><br/></td><td>
Renamed as per naming convention. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowDragDrop<br/><br/></td><td>
allowDragAndDrop<br/><br/></td><td>
Renamed as per naming convention.<br/><br/></td></tr>
<tr>
<td>
Events<br/><br/></td><td>
appointmentSaved<br/><br/></td><td>
beforeAppointmentCreate<br/><br/></td><td>
Renamed as per naming convention.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
appointmentEdited<br/><br/></td><td>
beforeAppointmentChange<br/><br/></td><td>
Renamed as per naming convention.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
appointmentDeleted<br/><br/></td><td>
beforeAppointmentRemove<br/><br/></td><td>
Renamed as per naming convention.<br/><br/></td></tr>
</table>