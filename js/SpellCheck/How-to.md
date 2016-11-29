---
title: How-to
description: Custom Configuration with SpellCheck control
platform: js
control: spellcheck
documentation: ug
keywords: spellcheck provider, NHunspell , ASpell, provider
---
# How To

## Using the nHunspell provider with SpellCheck control

The EJ SpellCheck supports the nHunspell and ASpell provider dictionary files to find and highlight misspell  words.

### ASpell provider

The ASpell provider support process similar to the Syncfusion base assembly reference process and the only difference is the dictionary file. While using the Syncfusion base assembly need to refer the default.dic file where as 
need to refer the ASpell.txt file to support the ASpell provider.

The following code example depicts the way to use the SpellCheck with ASpell provider dictionary file.

{% highlight c# %}

        SpellCheckController()
        {
            if (baseDictionary == null)
            {
                // Here we need to specify the corresponding file name
                string filePath = Path.Combine(AppDomain.CurrentDomain.BaseDirectory, @"Dictionary\", "ASpell.txt");
                Stream stream = new FileStream(filePath, FileMode.Open, FileAccess.Read);
                baseDictionary = new SpellCheckerBase(stream);
            }
            this.CustomFileRead();
        }

{% endhighlight %}

### NHunspell Provider

The EJ SpellCheck supports the NHunspell provider to perform the spellcheck operations. For this, need to follow the below steps.

Step 1: Load the required dictionary files by using the following code example in the controller page.

{% highlight c# %}

        private const string VirtualDictionaryPath = "~/ProviderDictionary/";
        private string _language;
        private readonly Hunspell _spell = new Hunspell();
        SpellCheckProviderController()
        {
            if (_spell.IsDisposed)
            {
                // culture name of the dictionary file
                Language = "en-US";
                string path = System.Web.HttpContext.Current.Server.MapPath(VirtualDictionaryPath + Language.Replace("-", "_"));
                // calling the load method with the dictionary files as arguments
                _spell.Load(path + ".aff", path + ".dic");
            }
        }


{% endhighlight %}

Step 2: Define the CheckWords, SplitWords and GetItems method with the following code examples.

{% highlight c# %}

        [AcceptVerbs("Get")]
        [ScriptMethod(ResponseFormat = ResponseFormat.Json)]
        public object CheckWords(string callback, string data)
        {
            var serializer = new JavaScriptSerializer();
            Actions args = (Actions)serializer.Deserialize(data, typeof(Actions));
            // Here calling the SplitWords method to separate the text and checking its erroneous
            var errorWordsCollection = this.SplitWords(args.text); 
            HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(errorWordsCollection)));
            return string.Empty;
        }


        private readonly List<SuggestionList> _items = new List<SuggestionList>();
        // Split words method to split the input string and checking the erroneous
        private List<SuggestionList> SplitWords(string text)
        {
            var words = text.Split(null);
            foreach (var word in words)
            {
                string textWord;
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
                this.GetItems(textWord);
            }

            return _items;
        }
        
        // Private method to form the error word collection list
        private List<SuggestionList> GetItems(string textWord)
        {
            var splitWords = Regex.Replace(textWord, @"[^0-9a-zA-Z\'_]", " ").Split(null);
            foreach (var inputWord in splitWords)
            {
                if (!this.CheckWord(inputWord))
                {
                    _items.Add(new SuggestionList
                    {
                        ErrorWord = inputWord,
                        SuggestedWords = this.GetSuggestions(inputWord)
                    });
                }
            }
            return _items;
        }
{% endhighlight %}

Step 3: Define the below methods to check the word erroneous and get an error words suggestions

{% highlight c# %}

        // Here passing the word to NHunspell method to check its erroneous
        private bool CheckWord(string word)
        {
            return _spell.Spell(word);
        }
        // Here passing the word to NHunspell method to check its suggestions
        private string[] GetSuggestions(string word)
        {
            return _spell.Suggest(word).ToArray();
        }


{% endhighlight %}

Step 4: To perform the add to dictionary operations define the method "AddToDictionary" with the following code example.

{% highlight c# %}

        [AcceptVerbs("Get")]
        [ScriptMethod(ResponseFormat = ResponseFormat.Json)]
        public object AddToDictionary(string callback, string data)
        {
            var serializer = new JavaScriptSerializer();
            Actions args = (Actions)serializer.Deserialize(data, typeof(Actions));
            if (args.CustomWord != null)
            {
                // Here calling the NHunspell add method to include custom word into the dictionary
                _spell.Add(args.CustomWord);
            }
            HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(args.customWord)));
            return string.Empty;
        }

{% endhighlight %}

Step 5: Add the following property definition code example to avoid the method accessibility errors.

{% highlight c# %}

        private string Language
        {
            get
            {
                return _language;
            }
            set
            {
                _language = value;
            }
        }
        
        public class SuggestionList
        {
            public string ErrorWord { get; set; }
            public string[] SuggestedWords { get; set; }
        }

        public class Actions
        {
            public string Text { get; set; }
            public string CustomWord { get; set; }
        }

{% endhighlight %}

N> Add the above code example changes in the server side file. For example, ejservices ->webapi->SpellChecker-> SpellCheckController 