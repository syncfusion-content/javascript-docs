---
layout: post
title: Exporting
description: exporting
platform: js
control: Grid
documentation: ug
---

# Exporting

Grid have support for exporting grid data to Excel, Word and Pdf file. Grid can be exported using `export` function, with export mapper as the parameter. Export can be added to UI in grid toolbar. The toolbar have option as `ExcelExport`, `WordExport` and `PdfExport` that are used to perform exporting. When you click the toolbar exporting icon, it internally invokes the `export` method.

Currently grid data can be converted to different file formats in server-side only through our helper functions in `.Net`. So, to use exporting in your projects, it is required to create a server with any of the following.
1.	ASP.Net MVC Controller Action
2.	ASP.Net Webforms WebMethod
3.	WebAPI
4.	WCF Service

Following code snippet demonstrate exporting with WebAPI controller.


{% highlight html %}


   <div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          dataSource: ej.DataManager({ url: "/api/Orders/", offline: true ,adaptor:”WebApiAdaptor”}),
          allowPaging: true,
          allowSorting: true,
          toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.ExcelExport, ej.Grid.ToolBarItems.WordExport,
               ej.Grid.ToolBarItems.PdfExport] },

          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 , textAlign: ej.TextAlign.Right },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                  { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ],
          toolbarClick: function (e) {
              this.exportGrid = this["export"];
              if (e.itemName == "Excel Export") {
                  this.exportGrid('/api/Orders/ExcelExport')
                  e.cancel = true;
              }
              else if (e.itemName == "Word Export") {
                  this.exportGrid('/api/Orders/WordExport')
                  e.cancel = true;
              }
              else if (e.itemName == "PDF Export") {
                  this.exportGrid('/api/Orders/PdfExport')
                  e.cancel = true;
              }
          },
      });
  });
</script>
{% endhighlight %}

{% highlight c# %}
public class OrdersController : ApiController
    {
        NORTHWNDEntities db = new NORTHWNDEntities();

        public IEnumerable<Order> Get()
        {
            return db.Orders.ToList();

        }

        [System.Web.Http.ActionName("ExcelExport")]
        [AcceptVerbs("POST")]
        public void ExcelExport()
        {
            string gridModel = HttpContext.Current.Request.Params["GridModel"];
            GridProperties gridProperty = ConvertGridObject(gridModel);
            ExcelExport exp = new ExcelExport();
            IEnumerable<Order> result = db.Orders.ToList();
            exp.Export(gridProperty, result, "Export.xlsx", ExcelVersion.Excel2010, false, false, "flat-saffron");


        }
        [System.Web.Http.ActionName("PdfExport")]
        [AcceptVerbs("POST")]
        public void PdfExport()
        {
            string gridModel = HttpContext.Current.Request.Params["GridModel"];
            GridProperties gridProperty = ConvertGridObject(gridModel);
            PdfExport exp = new PdfExport();
            IEnumerable<Order> result = db.Orders.ToList();
            exp.Export(gridProperty, result, "Export.pdf");


        }
        [System.Web.Http.ActionName("WordExport")]
        [AcceptVerbs("POST")]
        public void WordExport()
        {
            string gridModel = HttpContext.Current.Request.Params["GridModel"];
            GridProperties gridPropert = ConvertGridObject(gridModel);
            WordExport exp = new WordExport();
            IEnumerable<Order> data = db.Orders.ToList();
            exp.Export(gridPropert, (IEnumerable)data, "Export.docx");
        }
        private GridProperties ConvertGridObject(string gridProperty)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();
            IEnumerable div = (IEnumerable)serializer.Deserialize(gridProperty, typeof(IEnumerable));
            GridProperties gridProp = new GridProperties();
            foreach (KeyValuePair<string, object> ds in div)
            {
                var property = gridProp.GetType().GetProperty(ds.Key, BindingFlags.Instance | BindingFlags.Public | BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(ds.Value);
                    object value = serializer.Deserialize(serialize, type);
                    property.SetValue(gridProp, value, null);
                }
            }
            return gridProp;
        }


{% endhighlight %}



