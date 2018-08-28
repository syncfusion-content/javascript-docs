---
layout: post
title: webAPI reference for ejSpellCheck
description: webAPI reference for ejSpellCheck
documentation: ug
platform: js
keywords: spellcheck, ejspellcheck, syncfusion, spellcheck api
---

## CheckWords

It is used for splitting the input string into separate words and checking whether it is an erroneous word or not. Also, it forms a list of error words and its corresponding suggestions as a collection.  

### URL parameters

|  Parameter |  Description | 
|---|---|
|data|It contains target text, ignoreSettings values.| 

### Response information 

Code: 200

Content-Type: application/json; charset=utf-8 

Input:  Facebook is a social networking service headquartered in Menlo Park, California. Its website was launched on February 4, 2004, by Mark Zuckerberg with his Harvard College roommates and fellow students Eduardo, Andrew McCollum, Dustin and Chris Hughes.
The fouders had initially limited the websites membrship to Harvard students, but later expanded it to collges in the Boston area, the Ivy League, and Stanford Univrsity. It graually added support for students at various other universities and later to high-school students.

Response (JSON):   

Error Word Check and Highlight:

{% highlight js %}

// Response while requesting the jsonp type

[{"ErrorWord":"Facebook"},{"ErrorWord":"Zuckerberg"},{"ErrorWord":"fouders"},{"ErrorWord":"membrship"},{"ErrorWord":"collges"},{"ErrorWord":"Univrsity"},{"ErrorWord":"graually"}]

// Response while requesting the json type

"[{\"ErrorWord\":\"Facebook\"},{\"ErrorWord\":\"Zuckerberg\"},{\"ErrorWord\":\"fouders\"},{\"ErrorWord\":\"membrship\"},{\"ErrorWord\":\"collges\"},{\"ErrorWord\":\"Univrsity\"},{\"ErrorWord\":\"graually\"}]"

{% endhighlight %}

Suggestions for an Error Word:

{% highlight js %}

// Response while requesting the jsonp type

{"Facebook":[]}, 
{"Zuckerberg":[]},
{"fouders":["founders","fodders","folders","fosters","fouler","founder","founder\u0027s","fodder","fodder\u0027s","folder","folder\u0027s","fonder","footers","forgers","formers","foundered","founds","focuser","fondues","fondue\u0027s"]},
{"membrship":["membership","memberships","membership\u0027s","members"]},
{"collges":["collages","colleges","collies","collagen","collage\u0027s","collars","collates","colleens","college","college\u0027s","collides","collie","collied","collier","colliers","collie\u0027s","colludes","colognes","collagen\u0027s","collapse","collapses","collects","collier\u0027s","collapsed","collegian","collegians","collegiate"]},
{"Univrsity":["University","University\u0027s","Univariate","Universities","Unvisited"]},
{"graually":["gradually","gravelly","gradual","graduals","granularly"]}

// Response while requesting the json type

"{\"Facebook\":[]}"
"{\"Zuckerberg\":[]}"
"{\"fouders\":[\"founders\",\"fodders\",\"folders\",\"fosters\",\"fouler\",\"founder\",\"founder's\",\"fodder\",\"fodder's\",\"folder\",\"folder's\",\"fonder\",\"footers\",\"forgers\",\"formers\",\"foundered\",\"founds\",\"focuser\",\"fondues\",\"fondue's\"]}"
"{\"membrship\":[\"membership\",\"memberships\",\"membership's\",\"members\"]}"
"{\"collges\":[\"collages\",\"colleges\",\"collies\",\"collagen\",\"collage's\",\"collars\",\"collates\",\"colleens\",\"college\",\"college's\",\"collides\",\"collie\",\"collied\",\"collier\",\"colliers\",\"collie's\",\"colludes\",\"colognes\",\"collagen's\",\"collapse\",\"collapses\",\"collects\",\"collier's\",\"collapsed\",\"collegian\",\"collegians\",\"collegiate\"]}"
"{\"Univrsity\":[\"University\",\"University's\",\"Univariate\",\"Universities\",\"Unvisited\"]}"
"{\"graually\":[\"gradually\",\"gravelly\",\"gradual\",\"graduals\",\"granularly\"]}"

{% endhighlight %}

The error word suggestion request will be sending for each word and getting its result as shown in the above response respectively for each error word.

### Code example 

{% highlight js %}

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

{% endhighlight %}

{% highlight c# %}
        // Triggers while requesting the jsonp type
        [AcceptVerbs("Get","Post")]
        [ScriptMethod(ResponseFormat = ResponseFormat.Json)]
        public object CheckWords(string callback, string data)
        {
            var serializer = new JavaScriptSerializer();
            Actions args = (Actions)serializer.Deserialize(data, typeof(Actions));
            if (args.RequestType == "checkWords")
            {
                baseDictionary.IgnoreAlphaNumericWords = args.Model.IgnoreAlphaNumericWords;
                baseDictionary.IgnoreEmailAddress = args.Model.IgnoreEmailAddress;
                baseDictionary.IgnoreMixedCaseWords = args.Model.IgnoreMixedCaseWords;
                baseDictionary.IgnoreUpperCaseWords = args.Model.IgnoreUpperCase;
                baseDictionary.IgnoreUrl = args.Model.IgnoreUrl;
                baseDictionary.IgnoreFileNames = args.Model.IgnoreFileNames;
                var errorWords = this.SplitWords(args.Text);
                HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(errorWords)));
            }
            else if (args.RequestType == "getSuggestions")
            {
                var suggestions = baseDictionary.GetSuggestions(args.ErrorWord);                
                HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(suggestions)));
            }
            return string.Empty;                        
        }

        // Triggers while requesting the json type
        [AcceptVerbs("Get", "Post")]
        public object CheckWords(string data)
        {
            var serializer = new JavaScriptSerializer();
            Actions args = (Actions)serializer.Deserialize(data, typeof(Actions));
            if (args.RequestType == "checkWords")
            {
                baseDictionary.IgnoreAlphaNumericWords = args.Model.IgnoreAlphaNumericWords;
                baseDictionary.IgnoreEmailAddress = args.Model.IgnoreEmailAddress;
                baseDictionary.IgnoreMixedCaseWords = args.Model.IgnoreMixedCaseWords;
                baseDictionary.IgnoreUpperCaseWords = args.Model.IgnoreUpperCase;
                baseDictionary.IgnoreUrl = args.Model.IgnoreUrl;
                baseDictionary.IgnoreFileNames = args.Model.IgnoreFileNames;
                var errorWordsCollection = this.SplitWords(args.Text);
                return JsonConvert.SerializeObject(errorWordsCollection);
            }
            else if (args.RequestType == "getSuggestions")
            {
                var arr = baseDictionary.GetSuggestions(args.ErrorWord);
                return JsonConvert.SerializeObject(arr);
            }
            return "";
        }
{% endhighlight %}

## AddToDictionary

It is used to add the custom word into the custom dictionary file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|data|It contains custom word value.| 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Input:

{% highlight js %}
{customWord: “textarea”}
{% endhighlight %}

Output:   

{% highlight js %}
// Response while requesting the jsonp type
“textarea”

// Response while requesting the json type
"\"textarea\""
{% endhighlight %}

### Code example 

{% highlight js %}

$(function () {
    $("#TextArea").ejSpellCheck({
        dictionarySettings: {
	        dictionaryUrl: "https://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
	        customDictionaryUrl: "https://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
        }
    });
    
    $("#SpellCheck").ejButton({ width: "200px", height: "25px", click: "showDialog", text: "Spell check using dialog" });
});

function showDialog() {
    var spellObj = $("#TextArea").data("ejSpellCheck");
    spellObj.showInDialog();
}

{% endhighlight %}

{% highlight c# %}
        // Triggers while requesting the jsonp type
        [AcceptVerbs("Get","Post")]
        [ScriptMethod(ResponseFormat = ResponseFormat.Json)]
        public object AddToDictionary(string callback, string data)
        {
            var serializer = new JavaScriptSerializer();
            Actions args = (Actions)serializer.Deserialize(data, typeof(Actions));
            if (args.CustomWord != null)
            {
                this.AddToCustomDictionary(args.CustomWord);
            }
            HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(args.CustomWord)));
            return string.Empty;
        }

        // Triggers while requesting the json type
        [AcceptVerbs("Get", "Post")]
        public object AddToDictionary(string data)
        {
            var serializer = new JavaScriptSerializer();
            var args = (Actions)serializer.Deserialize(data, typeof(Actions));
            if (args.CustomWord != null)
            {
                AddToCustomDictionary(args.CustomWord);
            }
            return JsonConvert.SerializeObject(args.CustomWord);
        }

{% endhighlight %}

>The above code example shows that it is used to add the custom word into the custom dictionary file in SpellCheck component.

You need to include the following helper classes and SpellModel code examples to get the proper result while calling the above methods.

Helper Classes:

{% highlight c# %}
        
        private void CustomFileRead()
        {
            Stream stream1 = new FileStream(_customFilePath, FileMode.Open, FileAccess.ReadWrite);
            customDictionary = new SpellCheckerBase(stream1);
        }
        private bool CheckWord(string word)
        {
            var flag = false;
            if (baseDictionary.HasError(word))
            {
                flag = true;
                using (StreamReader sr = new StreamReader(_customFilePath))
                {
                    var contents = sr.ReadToEnd();
                    if (contents != "")
                    {
                        flag = customDictionary.HasError(word) ? true : false;
                    }
                }
            }
            return flag;
        }        
        private void AddToCustomDictionary(string word)
        {
            using (System.IO.StreamWriter file = new System.IO.StreamWriter(_customFilePath, true))
            {
                file.Write(word + Environment.NewLine);
            }
            this.CustomFileRead();
        }
        private List<Status> SplitWords(string text)
        {
            var words = text.Split(null);
            foreach (var word in words)
            {
                string textWord;
                Uri uriResult;
                bool checkUrl = Uri.TryCreate(word, UriKind.Absolute, out uriResult)
                              && (uriResult.Scheme == Uri.UriSchemeHttp || uriResult.Scheme == Uri.UriSchemeHttps);
                if (checkUrl)
                {
                    textWord = word;
                    if (this.CheckWord(textWord))
                    {
                        this.GetStatus(textWord);
                    }
                }
                else if (Regex.IsMatch(word,
                    @"^(?("")("".+?(?<!\\)""@)|(([0-9a-z]((\.(?!\.))|[-!#\$%&'\*\+/=\?\^`\{\}\|~\w])*)(?<=[0-9a-z])@))" +
                    @"(?(\[)(\[(\d{1,3}\.){3}\d{1,3}\])|(([0-9a-z][-\w]*[0-9a-z]*\.)+[a-z0-9][\-a-z0-9]{0,22}[a-z0-9]))$",
                    RegexOptions.IgnoreCase))
                {
                    textWord = word;
                    if (this.CheckWord(textWord))
                    {
                        this.GetStatus(textWord);
                    }
                }
                else if(Regex.IsMatch(word, @"[a-zA-Z0-9_$\-\.\\]*\\[a-zA-Z0-9_$\-\.\\]+"))
                {
                    textWord = word;
                    if (this.CheckWord(textWord))
                    {
                        this.GetStatus(textWord);
                    }
                }
                else
                {
                    if (word.EndsWith(".") || word.EndsWith(","))
                    {
                        textWord = word.Remove(word.Length - 1);
                    }
                    else if (word.Contains('\t') || word.Contains('\n') || word.Contains('\r'))
                    {
                        textWord = Regex.Replace(word, @"\t|\n|\r", "");
                    }
                    else
                    {
                        textWord = word;
                    }
                    this.GetStatus(textWord);
                }
            }
            return errorWords;
        }
        private List<Status> GetStatus(string textWord)
        {
            var splitWords = Regex.Replace(textWord, @"[^0-9a-zA-Z\'_]", " ").Split(null);
            foreach (var inputWord in splitWords)
            {
                if (this.CheckWord(inputWord))
                {
                    errorWords.Add(new Status
                    {
                        ErrorWord = inputWord
                    });
                }
            }
            return errorWords;
        }       

{% endhighlight %}

SpellModel Class Definition :

{% highlight c# %}

    public class SpellModel
    {
        public Boolean IgnoreAlphaNumericWords { get; set; }
        public Boolean IgnoreEmailAddress { get; set; }
        public Boolean IgnoreMixedCaseWords { get; set; }
        public Boolean IgnoreUpperCase { get; set; }
        public Boolean IgnoreUrl { get; set; }
        public Boolean IgnoreFileNames { get; set; }
    }

    public class Actions
    {
        public string Text { get; set; }
        public string CustomWord { get; set; }
        public SpellModel Model { get; set; }
        public string RequestType { get; set; }
        public string ErrorWord { get; set; }
    }
    
    public class Status
    {
        public string ErrorWord { get; set; }
    }

{% endhighlight %}