# IdeaStorm

Add one initials-prefixed bullet per idea, no matter how immediately practical or not. Use sub-bullets for fleshing them out a bit.

* JG/WS: Add formal CORS support for VersionOne instances -- allow to be toggled in System Administration such that the admin can provide a proper `Access-Control-Allow-Origin` and related headers. See prior branch experiments here:  https://github.com/versionone/VersionOne.SDK.Experimental/tree/master/ApiInputTranslatorPlugins
* JG: What are the documentation hurdles that our own teammates in V1 Dev teams, Support, and Services face when trying to code against the API or support customers?
* JG: Within our existing Java, .NET, Python, and JavaScript API client, what's a quick win we can take to make a large number of people happier?
* AndrewS: GraphQL based support for querying v1
* MI/JG: Clear documentation examples included for all relationship based filters like SubsMeAndDown, etc
  * API documentation similar to Twitter, Google, Heroku with cURL examples embedded inline
  * JG: Runnable code samples on line -- See https://community.versionone.com/Developers/DekiScript_Testing and the corresponding GitHub code samples repo here: https://github.com/versionone/CommunitySite.CodeSamples/tree/master/CommunitySite.CodeSamples/rest-1.v1
* JG/MI: Query builder that generates URI for plugging into any SDK or curl
* JG/MI: Generate clients in all languages based on code generation like t4 templates maybe
* MI: Generate a client with intellisense from Meta query -- Could this be intelligently populated at runtime inside VS? See F# Type Providers for real-world examples: https://msdn.microsoft.com/en-us/library/hh156509.aspx
* JG: LINQ on top of meta?
* JG: oData support for meta (great for excel, the number one agile tool on Earth) http://www.odata.org/
* CW: JSON data schema for API results and queries http://jsonapi.org/
