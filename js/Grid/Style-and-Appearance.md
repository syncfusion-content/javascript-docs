---
layout: post
title: Styling and appearance
description: Styling and appearance
platform: js
control: Grid
documentation: ug
---
# Styling

## List of classes and its purposes

To modify Grid appearance, you need to override default CSS of Grid. Please find the list of CSS classes and its corresponding section in Grid. Also you have an option to create your own custom theme for all JavaScript controls using our [Theme Studio](http://js.syncfusion.com/themestudio/# "Theme Studio").

  <table>
        <tr>
            <th>
                Section<br /><br />
            </th>
            <th>
                CSS class<br /><br />
            </th>
            <th>
                Purpose of CSS class<br /><br />
            </th>
        </tr>
        <tr>
            <td rowspan="2">
                Root <br /><br />
            </td>
            <td>
                e-grid <br /><br />
            </td>
            <td rowspan="2">
                This classes are in this root element (div) of grid control. <br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-js<br /><br />
            </td>
           
        </tr>
        <tr>
            <td rowspan="5">
                Header<br /><br />
            </td>
            <td>
                e-gridheader<br /><br />
            </td>
            <td>
                This is class is added in the root element of header element. In this class, You can override thin line between header and content of grid.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-table<br /><br />
            </td>
            <td>
                This class is added at 'table' of grid header. This CSS class makes table width as 100 %.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-columnheader<br /><br />
            </td>
            <td>
                This class is added at 'tr' of grid header. <br /><br />
            </td>
        </tr>
        <tr>
          
            <td>
                e-headercell<br /><br />
            </td>
            <td>
                This class is added in 'th' element of grid header. You can override background color of header and border color<br /><br />
            </td>
        </tr>
        <tr>
           
            <td>
                e-headercelldiv<br /><br />
            </td>
            <td>
                This class is add in div which present 'th' element in header. You recommend you to use e-headercelldiv to override skeleton of header.<br /><br />
            </td>
        </tr>
        <tr>
            <td rowspan="7">
                Body<br /><br />
            </td>
            <td>
                e-gridcontent<br /><br />
            </td>
            <td>
                This class is added at root of body content. This is to override background color of body.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-table<br /><br />
            </td>
            <td>
                This class is added to table of content. This CSS class makes table width as 100 %.<br /><br />
            </td>
        </tr>
        <tr>
           
            <td>
                e-alt_row<br /><br />
            </td>
            <td>
                This class is added to alternate rows of grid. This is to override alternate row color of grid.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-rowcell<br /><br />
            </td>
            <td>
                This class is added to all cells in grid. This is to override cells appearance and styling.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-groupcaption<br /><br />
            </td>
            <td>
                This class is added to 'td' of group caption which is to change background color of caption cell.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-selectionbackground<br /><br />
            </td>
            <td>
                This class is added to rowcell's of grid. this is override selection.<br /><br />
            </td>
        </tr>
        <tr>
          
            <td>
                e-hover <br /><br />
            </td>
            <td>
                This class adds to row of grid while hover grid rows.<br /><br />
            </td>
        </tr>
        <tr>
            <td rowspan="3">
                Pager<br /><br />
            </td>
            <td>
                e-pager<br /><br />
            </td>
            <td>
                This class is added to root element of pager. This to change appearance of background color and color of font.<br /><br />
            </td>
        </tr>
        <tr>
            
            <td>
                e-pagercontainer<br /><br />
            </td>
            <td>
                This class is added to numeric items of pager.<br /><br />
            </td>
        </tr>
        <tr>
          
            <td>
                e-parentmsgbar<br /><br />
            </td>
            <td>
                This class is added to pager info of pager.<br /><br />
            </td>
        </tr>
        <tr>
            <td rowspan="4">
                Summary<br /><br />
            </td>
            <td>
                e-gridfooter<br /><br />
            </td>
            <td>
                This class is added to root of summary div.<br /><br />
            </td>
        </tr>
        <tr>
          
            <td>
                e-gridsummary<br /><br />
            </td>
            <td>
                This class is added to table of summary. This CSS class makes table width as 100 %.<br /><br />
            </td>
        </tr>
        <tr>
          
            <td>
                e-gridSummaryRows<br /><br />
            </td>
            <td>
                This class is added to rows of grid summary. <br /><br />
            </td>
        </tr>
        <tr>
            <td>
                e-summaryrow<br /><br />
            </td>
            <td>
                This class is added to cells of summary row. This to override background color of summary.<br /><br />
            </td>
        </tr>
    </table>


## Toolbar Customization

To customize toolbar, you need to use toolbar default CSS class to override icon in toolbar. 

{% seealso %} [customize toolbar ](http://www.syncfusion.com/kb/5076/how-to-change-custom-icons-for-default-edit-toolbar-items "customize toolbar") {% endseealso %}

