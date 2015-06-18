---
layout: post
title: Angular-Support
description: angular support 
platform: js
control: Ribbon
documentation: ug
---

# Angular Support 

**Ribbon** control has angular support. It is possible to add object, array collection in the Ribbon control. The one way binding support is provided for Ribbon control. **ej-Ribbon** is the control tag where, ej is tag prefix and Ribbon is the control name.

To know more details about the Angular binding, refer to the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

## Rendering Tabs and Contextual tabs

Ribbon tabs and Contextual tabs are Array Collections and the inner tag is used for them. You can extend the Object with in these Array Collections by using hyphen. 

Ribbon tab and Contextual Tab are rendered with the following code example.

{% highlight html %}
 
    <div ng-app="ribbonApp">
       <div ng-controller="RibbonCtrl">
          <div id="defaultRibbon" ej-ribbon e-width="100%" e-applicationtab-itemid="ribbonmenu" e-applicationtab-type="ApplicationMenu">
             <div e-tabs>
                <div e-tab e-id="home" e-text="HOME">
                   <div e-groups>
                      <div e-group e-text="New" e-aligntype="rows">
                         <div e-content>
                            <div e-content e-defaults-type="button" e-defaults-width="60" e-defaults-height="70">
                               <div e-groups>
                                  <div e-group e-id="new" e-text="New">
                                  </div>
                               </div>
                            </div>
                         </div>
                      </div>
                   </div>
                </div>
             </div>
             <div e-contextualtabs>
                <div e-contextualtab e-backgroundcolor="#FCFBEB" e-bordercolor="#F2CC1C">
                   <div e-tabs>
                      <div e-tab e-id="Design" e-text="DESIGN">
                         <div e-groups>
                            <div e-group e-text="New" e-aligntype="rows">
                               <div e-content>
                                  <div e-content e-defaults-type="button" e-defaults-width="60" e-defaults-height="70">
                                     <div e-groups>
                                        <div e-group e-id="Design" e-text="Design">
                                        </div>
                                     </div>
                                  </div>
                               </div>
                            </div>
                         </div>
                      </div>
                   </div>
                </div>
             </div>
          </div>
          <ul id="ribbonmenu">
             <li>
                <a>FILE</a>
             </li>
          </ul>
       </div>
    </div>

{% endhighlight %}

After executing the above code, you can render the following output.

{% include image.html url="/js/Ribbon/Angular-Support_images/Angular-Support_img1.png" Caption="Ribbon Tab & Contextual tab with Angular JS"%}

## Rendering Gallery and Custom Tooltip

GalleryItems is an Array Collection and the inner tag is used for it inside the ribbon Groups. You can extend the Object of this Array Collection by using hyphen. Custom Tooltip is an Object of Ribbon Groups and you can extend it by using hyphen.

Eg: e-customtooltip-title.

Gallery and Custom Tooltip are rendered by using the following code example.

{% highlight html %}
   
      <div ng-app="ribbonApp">
         <div ng-controller="RibbonCtrl">
            <div id="defaultRibbon" ej-ribbon e-width="100%" e-applicationtab-itemid="ribbonmenu" e-applicationtab-type="ApplicationMenu" e-allowresizing="true">
               <div e-tabs>
                  <div e-tab e-id="home" e-text="HOME">
                     <div e-groups>
                        <div e-group e-text="New" e-aligntype="rows">
                           <div e-content>
                              <div e-content e-defaults-type="button" e-defaults-width="60" e-defaults-height="70">
                                 <div e-groups>
                                    <div e-group e-id="paste" e-text="Paste" e-customtooltip-title="Paste" e-customtooltip-content="<h6>Paste the content.<br &#47;><br &#47;>Add content on the Clipboard to your document.<&#47;h6>" e-customtooltip-prefixicon="e-pastetip">
                                    </div>
                                 </div>
                              </div>
                           </div>
                        </div>
                        <div e-group e-text="Gallery" e-aligntype="rows">
                           <div e-content>
                              <div e-content>
                                 <div e-groups>
                                    <div e-group e-id="Gallery" e-columns="3" e-itemheight="54" e-itemwidth="68" e-expandedcolumns="4" e-type="gallery">
                                       <div e-galleryitems>
                                          <div e-galleryitem e-text="GalleryContent1" e-buttonsettings-contenttype="imageonly" e-buttonsettings-prefixicon="e-gallerycontent1 e-gbtnimg" e-buttonsettings-cssclass="e-gbtnposition"></div>
                                          <div e-galleryitem e-text="GalleryContent2" e-buttonsettings-contenttype="imageonly" e-buttonsettings-prefixicon="e-gallerycontent2 e-gbtnimg" e-buttonsettings-cssclass="e-gbtnposition"></div>
                                          <div e-galleryitem e-text="GalleryContent3" e-buttonsettings-contenttype="imageonly" e-buttonsettings-prefixicon="e-gallerycontent3 e-gbtnimg" e-buttonsettings-cssclass="e-gbtnposition"></div>
                                       </div>
                                    </div>
                                 </div>
                              </div>
                           </div>
                        </div>
                     </div>
                  </div>
               </div>
            </div>
            <ul id="ribbonmenu">
               <li>
                  <a>FILE</a>
               </li>
            </ul>
         </div>
      </div>

{% endhighlight %}

After executing the above code, you can render the following output.

{% include image.html url="/js/Ribbon/Angular-Support_images/Angular-Support_img2.png" Caption="Ribbon Gallery & Custom Tooltip with Angular JS"%}

