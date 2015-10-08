---
layout: post
title: Localization
description: localization
platform: js
control: RichTextEditor
documentation: ug
---

# Localization

You can globalize the **RTE**, so that users of different cultures can make use of it and post their content. For your convenience, you can format the **RTE** control to your culture. When your blog is in your culture, the viewers of your culture can understand about your company and its products. You can achieve localization using the “**locale**” property. 

**RTE** support all the cultures. **Globalize.js** is a simple JavaScript library that allows you to use different cultures. Globalize cultures is the open source and you can get all the culture files from http://cdnjs.com/libraries/globalize/ link. 

In this example, **globalize.min.js** file is used that includes all the cultures information. And in this example **Spanish** culture is used. 

Add the following code in your **HTML** section to initialize the **RTE** with Spanish content.

{% highlight html %}

<div class="rte">
    <textarea id="rteSample">
        Control de RTE es un fácil de hacer en el lado del cliente .
        Cliente fácil de editar los contenidos y obtener el contenido HTML para el contenido mostrado .
        Un control de RTE proporciona a los usuarios una barra de herramientas que ayuda a aplicar formatos
        de texto enriquecido para el texto introducido en el área de texto .
    </textarea>
</div>

{% endhighlight %}

{% highlight js %}

    // Add the following code in your script section to render RTE with Spanish culture
    ej.RTE.Locale["es-ES"] = {
        bold: "audaz",
        italic: "itálico",
        underline: "subrayar",
        strikethrough: "Tachado",
        justifyCenter: "Centrar texto",
        justifyLeft: "Alinear texto a la izquierda",
        justifyRight: "Alinear texto a la derecha",
        justifyFull: "justificar",
        fileBrowser: "archivo Browser",
        unorderedList: "Inserte lista desordenada",
        orderedList: "Insertar lista ordenada",
        indent: "muesca",
        outdent: "anular sangria",
        undo: "deshacer",
        redo: "rehacer",
        clearAll: "Borrar todo",
        clearFormat: "Claro Formato",
        createLink: "Insertar / Editar hipervínculo",
        image: "insertar una imagen",
        video: "insertar vídeo",
        embedVideo: "Pegue su código de inserción por debajo de",
        viewHtml: "Ver HTML",
        format: "formato",
        deleteAlert: "¿Está seguro que desea borrar todo el contenido?",
        copyPastAlert: "Your browser doesn't support direct access to the clipboard. Please use the Ctrl+X/C/V keyboard shortcuts instead.",
        videoError: "El área de texto no puede estar vacío",
        imageWebUrl: "URL web",
        imageAltText: "Descripción",
        dimensions: "dimensiones",
        constrainProportions: "Restringir proporciones",
        linkWebUrl: "URL web",
        linkText: "texto",
        linkToolTip: "ToolTip",
        html5Support: "Este icono de la herramienta sólo disponible en HTML5 apoyó navegadores",
        linkOpenInNewWindow: "Abrir enlace en una nueva ventana",
        tableColumns: "Columnas No.of",
        tableRows: "Numero de Filas",
        tableWidth: "ancho de la mesa",
        tableHeight: "altura de la mesa",
        tableCellSpacing: "El espaciado",
        tableCellPadding: "Relleno",
        tableBorder: "frontera",
        tableCaption: "subtítulo",
        tableAlignment: "alineación",
        dialogUpdate: "actualización",
        dialogInsert: "insertar",
        dialogCancel: "cancelar",
        dialogOk: "bueno",
        createTable: "Crear una tabla",
        addColumnLeft: "Añadir la columna de la izquierda",
        addColumnRight: "Añadir columna a la derecha",
        addRowAbove: "Añadir fila encima",
        addRowBelow: "Añadir fila abajo",
        deleteRow: "Elimine la fila",
        deleteColumn: "Eliminar la columna",
        deleteTable: "Eliminar la tabla",
        customTable: "Crear una tabla personalizada",
        characters: "Personajes"
    };
    var format_ES = [
    { text: "acápite", value: "p", spriteCssClass: "e-paragraph" },
    { text: "cita", value: "blockquote", spriteCssClass: "e-quotation" },
    { text: "título 1", value: "h1", spriteCssClass: "e-h1" },
    { text: "título 2", value: "h2", spriteCssClass: "e-h2" },
    { text: "título 3", value: "h3", spriteCssClass: "e-h3" },
    { text: "título 4", value: "h4", spriteCssClass: "e-h4" },
    { text: "título 5", value: "h5", spriteCssClass: "e-h5" },
    { text: "título 6", value: "h6", spriteCssClass: "e-h6" }
    ];
    $(function () {
        $("#rteSample").ejRTE({
            width: "850px",
            showFooter: true,
            tools: {
                font: ["fontSize", "fontColor", "backgroundColor"],
                style: ["bold", "italic", "underline", "strikethrough"],
                alignment: ["justifyLeft", "justifyCenter", "justifyRight", "justifyFull"],
                lists: ["unorderedList", "orderedList"],
                copyPaste: ["cut", "copy", "paste"],
                doAction: ["undo", "redo"],
                clear: ["clearFormat", "clearAll"],
                links: ["createLink"],
                images: ["image", "video"],
                tables: ["createTable", "addRowAbove", "addRowBelow", "addColumnLeft", "addColumnRight", "deleteRow", "deleteColumn", "deleteTable"],
                scripts: ["superscript", "subscript"],
                casing: ["upperCase", "lowerCase"],
                paragraph: ["paragraph"]
            }
        });
    });

    $("#rteSample").ejRTE("model.format", format_ES);
    $("#rteSample").ejRTE("model.locale", "es-ES");

{% endhighlight %}


![]("/js/RichTextEditor/Localization_images/Localization_img1.png") 

