---
title: Globalization and Localization
description: Globalizing and localizing Scheduler
platform: js
control: schedule
documentation: ug
keywords: globalize, localize, localization, globalization 
---
# Globalization and Localization

## Globalization

The Scheduler control is built with default **globalization** support as it format the dates according to the user’s locale automatically and processes it internally without any need for manual conversions. This kind of default handling of Scheduler dates is achieved through the reference of **jQuery.globalize** library which globalizes the date, day and month names accordingly. 

## Localization

Scheduler also comes with default localization support which allows it to customize the display of text within the Scheduler in a user-specific culture and locale. The Schedule control can be localized in specific culture using the common API [locale](/js/api/ejschedule#members:locale) along with the collection of localized words defined for that culture using the ej.Schedule.Locale [**culture-code**].

**Note**: By default, the Schedule control is localized in **en-US** culture.

To localize Scheduler into a particular culture, it is necessary to refer the below specified scripts in your application,

* **jquery.globalize.min.js** 
* Other culture-specific script files, to which specific culture the Schedule needs to be adapted.

All the culture-specific script files are available under the following location – which needs to be referred in your application after the reference of the **jquery.globalize.min.js** file.                   

_<**Installed location**>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external\cultures\minified_

The following code example shows how to localize the Schedule control in **fr-FR** culture.

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

ej.Schedule.Locale["fr-FR"] = {

ReminderWindowTitle: "Fenêtre de rappel",

CreateAppointmentTitle: "créer un rendez-",

RecurrenceEditTitle: "Modifier répétition nomination",

RecurrenceEditMessage: "Comment voulez-vous changer le cas dans la série?",

RecurrenceEditOnly: "Seulement cette nomination",

RecurrenceEditSeries: "La série entière",

PreviousAppointment: "Nomination précédente",

NextAppointment: "prochain rendez-vous",

AppointmentSubject: "sujet",

StartTime: "Heure de début",

EndTime: "Heure de fin",

AllDay: "toute la journée",

Today: "aujourd'hui",

Recurrence: "répétition",

Done: "Terminé",

Cancel: "annuler",

Ok: "Ok",

RepeatBy: "Répétez par",

RepeatEvery: "répéter chaque",

RepeatOn: "répéter l'opération sur",

StartsOn: "démarre sur",

Ends: "extrémités",

Summary: "résumé",

Daily: "quotidien",

Weekly: "hebdomadaire",

Monthly: "mensuel",

Yearly: "annuel",

Every: "tous",

EveryWeekDay: "chaque jour de la semaine",

Never: "jamais",

After: "après",

Occurence: "apparition",

On: "sur",

Edit: "Modifier",

RecurrenceDay: "Jour (s)",

RecurrenceWeek: "Semaine (s)",

RecurrenceMonth: "Mois (s)",

RecurrenceYear: "Année (s)",

The: "la",

OfEvery: "de chaque",

First: "première",

Second: "deuxième",

Third: "troisième",

Fourth: "quatrième",

Last: "dernier",

WeekDay: "jour de la semaine",

WeekEndDay: "Jour de week-end",

Subject: "sujet",

Categorize: "Catégories",

DueIn: "En raison",

DismissAll: "rejeter tout",

Dismiss: "rejeter",

OpenItem: "Ouvrir l'élément",

Snooze: "répétition",

Day: "jour",

Week: "semaine",

WorkWeek: "Semaine de travail",

Month: "mois",

AddEvent: "Ajouter événement",

CustomView: "Vue personnalisée",

Agenda: "ordre du jour",

Detailed: "détaillé",

EventBeginsin: "Nomination commence dans",

Editevent: "Modifier nomination",

Editseries: "Modifier série",

Times: "fois",

Until: "jusqu'à",

Eventwas: "rendez-vous était",

Hours: "hrs",

Minutes: "minutes",

Overdue: "en retard",

Days: "jour (s)",

Event: "Sujet",

Select: "sélectionner",

Previous: "prev",

Next: "suivant",

Close: "proche",

Delete: "effacer",

Date: "date",

Showin: "montrer en",

Gotodate: "Aller à la date",

Resources: "RESSOURCES",

RecurrenceDeleteTitle: "Supprimer répétition rendez-",

Location: "emplacement",

Priority: "priorité",

RecurrenceAlert: "alerte",

WrongPattern: "Le modèle de récurrence est pas valable",

CreateError: "La durée de la nomination doit être plus courte que la façon dont elle se produit fréquemment. Raccourcir la durée ou changer le modèle de récurrence dans la boîte de dialogue Récurrence de rendez.",

DragResizeError: "Impossible de replanifier une occurrence du rendez-vous récurrent. si elle saute sur une occurrence ultérieure du même rendez-vous.",

StartEndError: "L'heure de fin doit être supérieur à l'heure de début",

MouseOverDeleteTitle: "supprimer un rendez-",

DeleteConfirmation: "Êtes-vous sûr de vouloir supprimer ce rendez-vous?",

Time: "Temps"

};

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

locale: "fr-FR",

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

Location: "CHINA"

}]

}

});

});

</script>



{% endhighlight %}

**Note**: Refer the **globalize.culture.fr-FR.min.js** file in your HTML application and also define the **locale** property for the Schedule control with the appropriate **culture-code** [**fr-FR**].

For further information on – how to refer the required culture scripts into your application, refer [here](/js/localization).

### Localizing Specific Words

To customize or localize only some specific words in the default `ej.Schedule.Locale["en-US"]` collection, the words to be localized/customized can be defined in a separate variable and then extended to the original collection as depicted in the following code example.

{% highlight html %}
<script>

var customizationMessage = {

// customize the appointment window title

CreateAppointmentTitle: "Create Event",

// customize the view options text in the Schedule header

Day: "1 Day",

Week: "7 Days",

WorkWeek: "5 Days",

Month: "Month"

};

// Extend only the required changes to the original locale collection

$.extend(ej.Schedule.Locale["en-US"], customizationMessage);

$(function () {

// defining Schedule control

$("#Schedule1").ejSchedule({

width: "100%",

height: "525px",

currentDate:new Date(2015,11,5),

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

}

});

});

</script>



{% endhighlight %}

## Time Zone

The Scheduler makes use of the System time zone by default. If it needs to be provided with some other user-specific time zone value, then the API [timeZone](/js/api/ejschedule#members:timezone) can be used. Also, the Scheduler can be set to observe the Daylight Saving Time (DST) with its **isDST** property which is set to **false** by default. 

When [isDST](/js/api/ejschedule#members:isdst) property is set to **true**, the Scheduler internally processes the time difference values (for the Start and end time of the appointments) related to the Scheduler time zone that observes daylight savings time. 

The following code example shows the way to set the specific time zone value with the daylight savings time observed in the Scheduler.

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

timeZone: "UTC +05:30",

isDST: true,

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

Location: "CHINA"

}]

}

});

});

</script>



{% endhighlight %}

Apart from the default Scheduler time zone, it is also possible to set the different time zone values for each appointments through the properties **startTimeZone** and **endTimeZone** which can be defined as separate fields within the appointment dataSource. When these properties are not explicitly defined for appointments, the appointments Start and End time will be processed based on the Scheduler time zone.

**Note**: The **isDST** property closely relies on the appointment fields like [StartTimeZone](/js/api/ejschedule#members:appointmentsettings-starttimezone) and [EndTimeZone](/js/api/ejschedule#members:appointmentsettings-endtimezone), for appropriate time difference calculations. If these two fields are not defined for appointments, then **isDST** depends on the System **timeZone** value.

The following code snippet shows how to define isDST and the time zones for specific appointments.

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

isDST: true,

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

Location: "CHINA",

StartTimeZone: "UTC +02:00",

EndTimeZone: "UTC +02:00"

}]

}

});

});

</script>



{% endhighlight %}

It is also possible to define or customize the default time zone collection of the Scheduler, by using the [timeZoneCollection](/js/api/ejschedule#members:timezonecollection) API as follows.

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

timeZoneCollection: {

dataSource: [

{ text: "UTC -04:00", id: "10", value: "UTC -04:00" },

{ text: "UTC -03:30", id: "11", value: "UTC -03:30" },

{ text: "UTC -03:00", id: "12", value: "UTC -03:00" },

{ text: "UTC -02:00", id: "13", value: "UTC -02:00" },

{ text: "UTC -01:00", id: "14", value: "UTC -01:00" },

{ text: "UTC +00:00", id: "15", value: "UTC +00:00" },

{ text: "UTC +01:00", id: "16", value: "UTC +01:00" },

{ text: "UTC +02:00", id: "17", value: "UTC +02:00" },

{ text: "UTC +03:00", id: "18", value: "UTC +03:00" },

{ text: "UTC +03:30", id: "19", value: "UTC +03:30" },

{ text: "UTC +04:00", id: "20", value: "UTC +04:00" },

{ text: "UTC +04:30", id: "21", value: "UTC +04:30" },

{ text: "UTC +05:00", id: "22", value: "UTC +05:00" }],

text: "text",

id: "id",

value: "value",

},

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

Location: "CHINA",

StartTimeZone: "UTC +02:00",

EndTimeZone: "UTC +02:00"

}]

}

});

});

</script>



{% endhighlight %}

**Note**: The values defined within the **timeZoneCollection** dataSource are usually the options displayed at the start and end time zone dropdown fields of the appointment window.

## Time Mode

The time mode of the Scheduler can be either **12** or **24 hours** format which is based on the [locale](/js/api/ejschedule#members:locale) set to the Scheduler. Since the default locale value of the Scheduler is **en-US**, therefore the time mode will be set to **12 hours** format (by default) automatically based on the culture. 

The user can also set specific time mode for the Scheduler using [timeMode](/js/api/ejschedule#members:timemode) property which accepts either **String** or **enum** value. It accepts the following **enum** values,

* ej.Schedule.TimeMode.Hour12
* ej.Schedule.TimeMode.Hour24

The following code snippet shows the way to set specific **24 hour format time mode** for the Scheduler.

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

timeMode: ej.Schedule.TimeMode.Hour24,

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

Location: "CHINA"

}]

}

});

});

</script>



{% endhighlight %}

**Note**: If the **timeMode** property is not set with specific value, then the value will be taken based on the locale assigned for the Scheduler.

## Date Format

Scheduler can be used with all valid date formats. The default date format used in Scheduler is “MM/dd/yyyy”. 

If the [dateFormat](/js/api/ejschedule#members:dateformat) property is not specified particularly, then it will be taken based on the locale that is assigned to the Scheduler. The default locale applied on the Scheduler is “en-US”, which makes it to follow the “MM/dd/yyyy” pattern by default.

{% highlight html %}


<div id="Schedule1"></div>



<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 5),

dateFormat: "yyyy/MM/dd",

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

}

});

});

</script>



{% endhighlight %}

