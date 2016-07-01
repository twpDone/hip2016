#OSInt

#Tool
? asin.py ?
By mkit Argentina
@matiasKatz

The tool is 100% free but you'll have to host it.
Tool is written in python.

You have many crawling choices like twitter, google, ...
It produce a *nice json* output

##Twitter
5 request / second

Just run the bot connect to the stream and provide a filter.
Twitter can filter *before* you get the stream

#Render your JSon
* Online maps provider
    * mysql DB
* Excel ::vomit::

You can use Google:
* Really easy API
* Great prefs
* cries when pushed too far

For example a google map 
The Geocoder works for us to draw countries, cities, ...

#Demo
`Web rendering`
A full functionally GMaps 
You can see the json produced by the maps API.

#Give some value
* Keyword match
* **Syntactic analysis**
* Manual Checks ? (Not)

#Python lib NLTK
For symbolic and syntactic analysis
* designed for 2.6 port to 3.2+
* Long but simple learning curve
* Awesomely good perfs

Do 
* Interpretation of sentences
* Information extraction
* Not an IA

> My house is beautiful but i don't like it
Is it a positive or a negative comment.
It's negative, and understanding that is the goal of NLTK

`pip install nltk` 
Wait ... (2GB)

Tokenizer:
* Create arrays with each part of the sentence.

You can check for frequency:
* N appearances per word
* Calculate repetions and gives values according to *weight*
* Perform analysis of entire sentence

You can classify your tweet, it return a value between 0 and 100 accpording to relevance.

`A look at the code`
2 month of babysit and learning time and you'll have a powerfull tool.

It's not a string match, it's an interpretation.

#No what
Live Map, which search for words an color the pointer if it's positive or negative.
`Prints Tweets in Maps (England, then worldwide) about Brexit`

7 second from tweet to print on the maps




