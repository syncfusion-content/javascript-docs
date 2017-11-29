---
layout: post
title: Accessibility Features of ComboBox widget for Syncfusion Essential JS
description: Describes about the accessibility in ComboBox widget for Syncfusion Essential JS.
platform: js
control: ComboBox
documentation: ug
keywords: ComboBox, ComboBox, Accessibility, ARIA attributes, Keyboard interaction
---

# Accessibility

The ComboBox component has been designed, keeping in mind the `WAI-ARIA` specifications, and applies the WAI-ARIA roles, states, and properties along with `keyboard support`. This component is characterized
by complete keyboard interaction support and ARIA accessibility support that makes it easy for people who use assistive technologies (AT) or those who completely rely on keyboard navigation.

## ARIA Attributes

The ComboBox component uses the `combobox` role, and each list item has an `option` role. The following `ARIA attributes` denote the ComboBox state.

| **Properties** | **Functionalities** |
| --- | --- |
| aria-haspopup | Indicates whether the ComboBox input element has a popup list or not. |
| aria-expanded | Indicates whether the popup list has expanded or not. |
| aria-selected | Indicates the selected option. |
| aria-readonly | Indicates the readonly state of the ComboBox element. |
| aria-disabled | Indicates whether the ComboBox component is in a disabled state or not. |
| aria-activedescendent | This attribute holds the ID of the active list item  to focus its descendant child element. |
| aria-owns | This attribute contains the ID of the popup list to indicate popup as a child element. |
| aria-autocomplete | This attribute contains the ‘both’ to a list of options shows and the currently selected suggestion also shows inline. |

## Keyboard Interaction

You can use the following key shortcuts to access the ComboBox without interruptions.

| **Keyboard shortcuts** | **Actions** |
| --- | --- |
| <kbd>Arrow Down</kbd> | Selects the first item in the ComboBox when no item selected. Otherwise, selects the item next to the currently selected item. |
| <kbd>Arrow Up</kbd> | Selects the item previous to the currently selected one. |
| <kbd>Page Down</kbd> | Scrolls down to the next page and selects the first item when popup list opens. |
| <kbd>Page Up</kbd> | Scrolls up to the previous page and selects the first item when popup list opens. |
| <kbd>Enter</kbd> | Selects the focused item and popup list closes when it is in open state. |
| <kbd>Tab</kbd> | Focuses on the next TabIndex element on the page when the popup is closed. Otherwise, closes the popup list and remains the focus of the component. |
| <kbd>Shift + tab </kbd> | Focuses on the previous TabIndex element on the page when the popup is closed. Otherwise, closes the popup list and remains the focus of the component. |
| <kbd>Alt + Down</kbd> | Open the popup list |
| <kbd>Alt + Up</kbd> | Close the popup list|
| <kbd>Esc(Escape)</kbd> | Closes the popup list when it is in an open state and the currently selected item remains the same. |
| <kbd>Home</kbd> | Selects the first item when popup open state. If it is in closed state, cursor moves to before of first character in input |
| <kbd>End</kbd> | Selects the last item when popup open state. If it is in closed state, cursor moves to next of last character in input  |

> In the following sample, focus the ComboBox component using <kbd>alt+t</kbd> keys.

{% highlight html %}
	
	 <input type="text" tabindex="1" id="list" />
			
{% endhighlight %}
	
{% highlight javascript %}	
	
    var sportsList = [
        { id: 'level1', country: 'American Football' }, { id: 'level2', country: 'Badminton' },
        { id: 'level3', country: 'Basketball' }, { id: 'level4', country: 'Cricket' },
        { id: 'level5', country: 'Football' }, { id: 'level6', country: 'Golf' },
        { id: 'level7', country: 'Hockey' }, { id: 'level8', country: 'Rugby' },
        { id: 'level9', country: 'Snooker' }, { id: 'level10', country: 'Tennis' }
    ];
    $(function () {
        $("#list").ejComboBox({
            dataSource: sportsList,
            fields: { text: 'country', value: 'id' },
            width: '250px',
            placeholder: 'Select a game',
            index: -1,
            popupHeight: '200px',
            popupWidth: '250px'
        });
    });
    $(document).on("keydown", function (e) {
        if (e.altKey && e.keyCode === 74) { // j- key code.
            $("#list").focus();
        }
    });	

{% endhighlight %}
