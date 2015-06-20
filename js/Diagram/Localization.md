---
layout: post
title: Localization
description: localization 
platform: js
control: Diagram
documentation: ug
---

# Localization 

Localization is the process of providing controls in different cultures, to help you set your own culture easily. Diagram provides localization support for Context Menu items. The following code illustrates how to provide localization support for Context Menu items.

{% highlight js %}

$("#DiagramContent").ejDiagram({            
    locale:"es-ES",
});

ej.datavisualization.Diagram.Locale["es-ES"] = {
    cut: "Corte",
    copy: "Copia",
    paste: "Pasta",
    undo: "Deshacer",
    redo: "Rehacer",
    selectAll: "Seleccionar todo",
    grouping: "Agrupación",
    group: "Grupo",
    ungroup: "Desagrupar",
    order: "Fin",
    bringToFront: "Traer a delante",
    moveForward: "Movimiento adelante",
    sendToBack: "Enviar a espalda",
    sendBackward: "Enviar hacia atrás"
};

{% endhighlight %}

{% include image.html url="/js/Diagram/Localization_images/Localization_img1.png" %}