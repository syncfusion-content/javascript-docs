---
layout: post
title: Localization
description: localization
platform: js
control: DateTimePicker
documentation: ug
---

# Localization

You can globalize your **DateTimePicker** control. People of different culture can make use of it. All culture files are supported by Syncfusion components

**Globalize.js** is a simple JavaScript library that allows you to format and parse numbers and dates in a culture-specific fashion. The globalize cultures is the open source and you can get all the culture files online. Refer the online link given,

[http://cdnjs.com/libraries/globalize/](http://cdnjs.com/libraries/globalize/)

You can get the script file of various cultures from the following path also:
**"&lt;Installed Location&gt;\** **Syncfusion** **\Essential Studio\&lt;version&gt;\JavaScript\assets\external\cultures**"

If you want to use any cultures, add the script files of those corresponding culture in the sample. In order to add UK Culture in the **DateTimePicker** you can refer a script file named "**globalize.culture.es-ES.js**". 

You can also customize the culture to your own, using the following steps.

* Open the **Culture** script file, included in your project.

* Replace existing calendar locale information by your own culture information or to your customized format.

Refer this section for more details: [localization](http://help.syncfusion.com/ug/js/default.htm)

For example, if you want to change month names to your culture month just replace month names with your culture month names or your customized format.

The following code example is used to know Spanish calendar locale information.

{% highlight js %}

calendars: {
              standard: {
                  firstDay: 1,
**days**: {
**names**: ["domingo","lunes","martes","miércoles","jueves","viernes","sábado"],
**namesAbbr**: ["do.","lu.","ma.","mi.","ju.","vi.","sá."],
**namesShort**: ["D","L","M","X","J","V","S"]
                  },
**months**: {
**names**: ["enero","febrero","marzo","abril","mayo","junio","julio","agosto","septiembre","octubre","noviembre","diciembre",""],
**namesAbbr**: ["ene.","feb.","mar.","abr.","may.","jun.","jul.","ago.","sep.","oct.","nov.","dic.",""]
                  },
                  AM: null,
                  PM: null,
                  eras: [{"name":"d. C.","start":null,"offset":0}],
                  patterns: {
                      d: "dd/MM/yyyy",
                      D: "dddd, d' de 'MMMM' de 'yyyy",
                      t: "H:mm",
                      T: "H:mm:ss",
                      f: "dddd, d' de 'MMMM' de 'yyyy H:mm",
                      F: "dddd, d' de 'MMMM' de 'yyyy H:mm:ss",
                      M: "d' de 'MMMM",
                      Y: "MMMM' de 'yyyy"
                  }
              }
      }



{% endhighlight %}



The following code example can be used to get Spanish culture in **DateTimePicker**.

Add the following code in your **HTML** page.


  {% highlight html %}

  **[HTML]**
  
     <div class="control">
	        <input type="text" id="dateTime" />
	    </div>


  {% endhighlight %}


  {% highlight js %}

  **[JavaScript]**
  
  // Adds the code in your script section to render the DateTimePicker with Spanish culture
  
	          $("#dateTime").ejDateTimePicker({
	              locale: "es-ES"
	          });


  {% endhighlight %}

{% include image.html url="/js/DateTimePicker/Concepts-and-Features/Localization_images/Localization_img1.png" Caption="Showcase for DateTimePicker with Spanish culture"%}

