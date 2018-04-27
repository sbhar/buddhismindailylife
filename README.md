# buddhismindailylife

Buddhism in Daily Life (json to dom)

JSON must be generated using domJSON.js by Alex Zaslavsky

Example code to convert to json
```
var jsonOutput = domJSON.toJSON(myDiv, {
	domProperties: [false, false, false],
	metadata: false
});

```
Example of converted JSON:
```
var jsonexample = '{"nodeType":1,"tagName":"DIV","attributes":{"class":"h-card col-3 float-left pr-3","id":"azaslavsky","align":"center"},"childNodes":[{"nodeType":1,"tagName":"DIV","attributes":{"class":"card h-100","id":"bg-18"},"childNodes":[{"nodeType":1,"tagName":"DIV","attributes":{"class":"view overlay hm-white-slight"},"childNodes":[{"nodeType":1,"tagName":"A","attributes":{"itemprop":"image","class":"u-photo d-block position-relative","aria-hidden":"true","href":"https://avatars1.githubusercontent.com/u/3709945?s=400&v=4"},"childNodes":[{"nodeType":1,"tagName":"IMG","attributes":{"src":"https://avatars0.githubusercontent.com/u/3709945?s=460&v=4"},"childNodes":[]}]},{"nodeType":1,"tagName":"BR","attributes":{},"childNodes":[]},{"nodeType":1,"tagName":"A","attributes":{"rel":"nofollow me","class":"u-url","href":"https://twitter.com/alex__zaslavsky"},"childNodes":[{"nodeType":3,"nodeValue":"https://twitter.com/alex__zaslavsky","childNodes":[]}]}]},{"nodeType":1,"tagName":"DIV","attributes":{"class":"card-body"},"childNodes":[{"nodeType":1,"tagName":"H4","attributes":{"class":"card-title"},"childNodes":[{"nodeType":1,"tagName":"B","attributes":{},"childNodes":[]}]},{"nodeType":1,"tagName":"P","attributes":{"class":"card-text"},"childNodes":[]},{"nodeType":1,"tagName":"A","attributes":{"class":"btn btn-primary","target":"_blank","href":"https://github.com/azaslavsky"},"childNodes":[{"nodeType":3,"nodeValue":"Read More","childNodes":[]}]}]}]}]}';
```

Example code to convert back to DOM html
```
var obj = $.parseJSON(jsonexample);
var DOMDocumentFragment = domJSON.toDOM(obj);
$('#anydivid').html(DOMDocumentFragment);
```