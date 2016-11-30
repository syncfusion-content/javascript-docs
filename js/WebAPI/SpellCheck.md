---
layout: post
title: webAPI reference for ejSpellCheck
description: webAPI reference for ejSpellCheck
documentation: API
platform: js-webapi
keywords: spellcheck, ejspellcheck, syncfusion, spellcheck api
---

## CheckWords

[GET/Api/SpellCheck/CheckWords](http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords)

It is used for splitting the input string into separate words and checking whether it is an erroneous word or not. Also, it forms a list of error words and its corresponding suggestions as a collection.  

### URL parameters

|  Parameter |  Description | 
|---|---|
| data  |It contains target text, ignoreSettings values. | 

### Response information 

Code: 200

Content-Type: application/json; charset=utf-8 

Input:  Facebook is a social networking service headquartered in Menlo Park, California. Its website was launched on February 4, 2004, by Mark Zuckerberg with his Harvard College roommates and fellow students Eduardo, Andrew McCollum, Dustin and Chris Hughes.
The fouders had initially limited the websites membrship to Harvard students, but later expanded it to collges in the Boston area, the Ivy League, and Stanford Univrsity. It graually added support for students at various other universities and later to high-school students.

Response (JSON):   

~~~ javascript
[
	{"ErrorWord":"Facebook","SuggestedWords":[]},{"ErrorWord":"Zuckerberg","SuggestedWords":[]},{"ErrorWord":"fouders","SuggestedWords":["founders","fodders","folders","fosters","fouler","founder","founder\u0027s","fodder","fodder\u0027s","folder","folder\u0027s","fonder","footers","forgers","formers","foundered","founds","focuser","fondues","fondue\u0027s"]},{"ErrorWord":"membrship","SuggestedWords":["membership","memberships","membership\u0027s","members"]},{"ErrorWord":"collges","SuggestedWords":["collages","colleges","collies","collagen","collage\u0027s","collars","collates","colleens","college","college\u0027s","collides","collie","collied","collier","colliers","collie\u0027s","colludes","colognes","collagen\u0027s","collapse","collapses","collects","collier\u0027s","collapsed","collegian","collegians","collegiate"]},{"ErrorWord":"Univrsity","SuggestedWords":["University","University\u0027s","Univariate","Universities","Unvisited"]},{"ErrorWord":"graually","SuggestedWords":["gradually","gravelly","gradual","graduals","granularly"]}
]

~~~ 

### Code example 

~~~ javascript

$(function () {
	$("#TextArea").ejSpellCheck({
		dictionarySettings: {
			dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords"
		}
	});
	$("#SpellCheck").ejButton({ width: "200px", height: "25px", click: "showDialog", text: "Spell check using dialog" });
});

function showDialog() {
	var spellObj = $("#TextArea").data("ejSpellCheck");
	spellObj.showInDialog();
}

~~~ 

## AddToDictionary

[GET/Api/SpellCheck/AddToDictionary](http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords)

It is used to add the custom word into the custom dictionary file.

### URL parameters

|  Parameter |  Description | 
|---|---|
| data  | It contains custom word value.| 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Input:

~~~ javascript
{customWord: “textarea”}
~~~ 

Output:   

~~~ javascript
“textarea”
~~~ 

### Code example 

~~~ javascript

$(function () {
	$("#TextArea").ejSpellCheck({
		dictionarySettings: {
			dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
			customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
		}
	});
	$("#SpellCheck").ejButton({ width: "200px", height: "25px", click: "showDialog", text: "Spell check using dialog" });
});

function showDialog() {
	var spellObj = $("#TextArea").data("ejSpellCheck");
	spellObj.showInDialog();
}

~~~ 

>The above code example shows that it is used to add the custom word into the custom dictionary file in SpellCheck component.