#SpectragramJS v.0.1
##An Instagram API plugin for jQuery

**spectragram.js** is a jQuery plugin using the **Instagram API** to fetch and display user, popular or tags photo feeds inside a list or any container you define.

#Features

* Get the most recent media published by a user, the most popular media at the moment, or recently tagged media from Instagram API
* Display the results on list items or any other HTML tag you define
* Define the size of the pictures (small, medium, big)
* Use your own Instagram application ClientID and AccessToken

#How to use

In order to use the plugin you need to register an application at [Instagram Developers](http://instagram.com/developer/), get a **client_id** and [recieve an access_token](http://instagram.com/developer/authentication/).

###Simple usage

1. Be sure to have jQuery script included and then include the **spectragram.js** script right before the ``` </body>``` tag.

```
 <script type="text/javascript" src="js/spectragram.js"></script>
```

2. Call the **spectragram function** on your script and set your Instagram ```accessToken```, ```clientID``` and the query:

```
$('ul').spectragram('getRecentTagged',{
	accessToken: '[your-instagram-access-token]',
	clientID: '[your-instagram-application-clientID]',
	query: 'converse'
});
```

*This example will show 10 or less results for photos tagged "converse" in a list, "medium" sized.*

##Configuration

```
.spectragram( Method, [Options] )

Method: getUserFeed, getPopular or getRecentTagged functions

Options: An array to configure the properties of spectragram
```
###Methods
**getUserFeed**  
Get the most recent media published by a user.

```
$('ul').spectragram('getUserFeed',{
	accessToken: '[your-instagram-access-token]',
	clientID: '[your-instagram-application-clientID]',
	query: 'adrianengine'
});
```

**getPopular**  
Get a list of what media is most popular at the moment.

```
$('ul').spectragram('getPopular',{
	accessToken: '[your-instagram-access-token]',
	clientID: '[your-instagram-application-clientID]'
});
```

**getRecentTagged**  
Get a list of recently tagged media.

```
$('ul').spectragram('getRecentTagged',{
	accessToken: '[your-instagram-access-token]',
	clientID: '[your-instagram-application-clientID]',
	query: 'converse'
});
```

###Options
**accessToken** (required)  
*Type: String*  
This is your Instagram Application AccessToken. *Default: Null*

**clientID** (required)  
*Type: String*  
This is your Instagram Application Client ID. *Default: Null*

**query** (required)   
*Type: String*  
The string to search. *Default: 'coffee'*

**max**  
*Type: Number*  
The maximum number of results to show. *Default: 10*

**size**  
*Type: String*  
The size of the photos. 'small', 'medium' or 'big'. *Default: 'medium'*

**wrapEachWith**  
*Type: String*  
The HTML tag to wrap every result. *Default: '\<li>\</li>'*

###Example
```
$('div').spectragram({
	accessToken: '[your-instagram-access-token]',
	clientID: '[your-instagram-application-clientID]',
	query: 'converse',
	max: 14,
	size: 'big',
	wrapEachWith: '<p></p>'}
});
```

#License

Dual licensed under the MIT or GPL Version 2 licenses. You are free to use this plugin in commercial projects as long as the copyright header is left intact.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE. 
 
#Changelog

v0.01 (2012-Jul-04) - Release

#Further notes
Developed by [Adrian Quevedo](http://adrianquevedo.com) at Núcleo Digital S.A.S, in Bogotá - Colombia.

This code is provided with no warranty. While I strive to maintain backwards compatibility, the code is still under active development. As this is the case, some revisions may break compatibility with earlier versions of the library. Please keep this in mind when using the plugin.

This plugin uses the Instagram(tm) API and is not endorsed or certified by Instagram or Burbn, inc. All Instagram(tm) trademarks displayed on this plugin are property of Burbn, Inc.