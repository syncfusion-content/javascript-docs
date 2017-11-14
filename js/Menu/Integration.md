---
layout: post
title: Integration
description: integration
platform: js
control: Menu
documentation: ug
api: /api/js/ejmenu
---

# Integration

## AngularJS binding

AngularJS is an open-source web application Framework. AngularJS extends **HTML** with new attributes. AngularJS is a **JavaScript** Framework. You can add it to an **HTML** page with a **&lt;script&gt;** tag. AngularJS extends **HTML** attributes with Directives, and binds data to **HTML** with Expressions. The support is achieved by an integration JS library file. You can know more about the AngularJS support in the following link location. 

<https://help.syncfusion.com/js/angularjs>

Sometime you can use menu value for retrieving information from the database by performing related action that is selected in menu. You can achieve this after the selected menu action is performed in the server side.

In the following example, a **Menu** control for mail application is created. In this, when you click **mail** **Inbox** **development**, the selected development value is sent to the database. Normally a mail database contains different type of mails like HR team, Accounts team, etc. Whereas, in this example, the mail from development team is only retrieved from the database. Then the result is updated in the necessary page.

Add the following code in your **HTML** page.

{% highlight html %}


<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="menuApp">
<head>
    <title>Essential Studio for JavaScript :  AngularJS</title>
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
</head>
<body ng-controller="MenuCtrl">

    <ul id="menu" ej-menu e-fields-datasource="dataList" e-fields-id="id" e-fields-parentid="parentId"
        e-fields-text="text" e-fields-spritecssclass="sprite">
    </ul>
</body>
</html>

{% endhighlight %}

{% highlight javascript %}

   
    // Initialize the control in JavaScript.
    var data = [
         { id: 1, text: "Mail", parentId: null },
         { id: 2, text: "Calender", parentId: null },
         { id: 3, text: "Notes", parentId: null },
         { id: 4, text: "Contacts", parentId: null },
         //first level child
         { id: 11, parentId: 1, text: "Inbox", sprite: "mail sprite-inbox" },
         { id: 12, parentId: 1, text: "Drafts", sprite: "mail sprite-drafts" },
         { id: 13, parentId: 1, text: "Sent items", sprite: "mail sprite-sentitems" },
         { id: 14, parentId: 1, text: "Deleted", sprite: "mail sprite-deleted" },
         { id: 15, parentId: 1, text: "Junk mails", sprite: "mail sprite-junk" },
         { id: 16, parentId: 1, text: "Personal", sprite: "mail sprite-folders" },
         { id: 17, parentId: 2, text: "My Calender", sprite: "mail sprite-calendar" },
         { id: 18, parentId: 2, text: "Team", sprite: "mail sprite-calendar" },
         { id: 19, parentId: 2, text: "Others", sprite: "mail sprite-calendar" },
         { id: 20, parentId: 3, text: "My Reference", sprite: "mail sprite-folder" },
         { id: 21, parentId: 3, text: "Team Meeting", sprite: "mail sprite-folder" },
         { id: 22, parentId: 3, text: "Others", sprite: "mail sprite-folder" },
         { id: 23, parentId: 4, text: "Suggested", sprite: "mail sprite-contacts" },
         { id: 24, parentId: 4, text: "My Team", sprite: "mail sprite-contacts" },
         { id: 25, parentId: 4, text: "Others", sprite: "mail sprite-contacts" },
         //second level child
         { id: 111, parentId: 11, text: "Development", sprite: "mail sprite-folders" },
         { id: 111, parentId: 11, text: "Supports", sprite: "mail sprite-folders" },
         { id: 111, parentId: 11, text: "HR Team", sprite: "mail sprite-folders" },
         { id: 112, parentId: 12, text: "Support Template", sprite: "mail sprite-folders" },
         { id: 112, parentId: 12, text: "Personal", sprite: "mail sprite-folders" }
    ];
    angular.module('menuApp', ['ejangular']).controller('MenuCtrl', function ($scope) {
        $scope.dataList = data;
    });


{% endhighlight %}

Add the following code in your style section.

{% highlight css %}


<style type="text/css">
    #menu {
        margin-left: 50px;
    }

    .e-menu li > ul > li > a {
        padding: 0 18px 0 28px;
    }

    [class^="sprite-"],
    [class*="sprite-"] {
        background-image: url("../images/mail/mails.png");
        height: 25px;
        left: 2px;
        top: 4px;
        width: 24px;
    }

    .sprite-drafts {
        background-position: 50px 407px;
    }

    .sprite-sentitems {
        background-position: 51px 376px;
    }

    .sprite-deleted {
        background-position: 50px 342px;
    }

    .sprite-junk {
        background-position: 51px 308px;
    }

    .sprite-inbox {
        background-position: 48px 478px;
    }

    .sprite-folders {
        background-position: 47px 26px;
    }

    .sprite-calendar {
        background-position: 49px 236px;
    }

    .sprite-folder {
        background-position: 50px 271px;
    }

    .sprite-contacts {
        background-position: 49px 62px;
    }
</style>


{% endhighlight %}



The following screenshot displays the output of the above code example.       

![](/js/Menu/Integration_images/Integration_img1.png) 


## KnockoutJS binding

**KnockoutJS** is a MVVM library that allows the separation of concerns. **Essential JavaScript** provides full support for KnockoutJS. The KnockoutJS support is achieved by an integration JS library file. Add the following code for KnockoutJS binding **Menu** rendering.

* When you use KO with your applications, you can get the following benefits. 
* You can connect **UI** elements with data model anytime. 
* You can easily create complex dynamic data model.  
* You can automatically update **UI** when Data Model is changed and when UI is changed,Data Model is changed automatically. 

In the following example, select Sign Up menu, the requested menu value is send to the server and you can render response from the server with Sign Up page. Here sign up and sign in page **UI** layout is totally different, and the data model is automatically changed.

Add the following code in your **HTML** page.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
</head>
<body>
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <ul id="menuko" data-bind="ejMenu :{fields:{dataSource:dataList,id:'id',text:'text',parentId:'parentId',spriteCssClass:'sprite'}}"></ul>
            </div>
        </div>
    </div>
  </body>
  </html>
{% endhighlight %}

{% highlight css %}

  
    // Initialize the control in JavaScript.
    $(document).ready(function () {
        // declaration
        var menu = [
            { id: 1, text: "Products", parentId: null },
            { id: 2, text: "Support", parentId: null },
            { id: 3, text: "Consulting", parentId: null },
            { id: 4, text: "Login", parentId: null },
            //first level child
            { id: 11, parentId: 1, text: "JS" },
            { id: 12, parentId: 1, text: "ASP.NET" },
            { id: 13, parentId: 1, text: "ASP.NET MVC" },
            { id: 14, parentId: 1, text: "Mobile" },
            { id: 15, parentId: 1, text: "WPF" },
            { id: 16, parentId: 2, text: "Direct Trac" },
            { id: 17, parentId: 2, text: "Community Forum" },
            { id: 18, parentId: 2, text: "Online Doc" },
            { id: 20, parentId: 3, text: "Online App" },
            { id: 21, parentId: 3, text: "Windows App" },
            { id: 22, parentId: 3, text: "Mobile App" },
            { id: 24, parentId: 3, text: "Servicing" },
            { id: 30, parentId: 4, text: "Sign Up" },
            { id: 32, parentId: 4, text: "Sign In" }
        ];

        window.viewModel = {
            dataList: ko.observableArray(menu),

        };
        ko.applyBindings(viewModel);
    });


{% endhighlight %}


Add the following code in your style section.

{% highlight css %}


<style type="text/css">
    #menuko {
        margin-left: 50px;
    }
    .e-menu li > ul > li > a {
        padding: 0 18px 0 26px;
    }
</style>   


{% endhighlight %}



The following screenshot displays the output of the above code.              

![](/js/Menu/Integration_images/Integration_img2.png) 


