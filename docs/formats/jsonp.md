# JSONP or JSON-P (JSON with Padding)

JSONP, or JSON-P (JSON with Padding), is a historical JavaScript technique for requesting data by loading a `<script>` element, which is an element intended to load ordinary JavaScript.

- [json-p.org](https://json-p.org){:target="_blank"}
- [en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP){:target="_blank"}

## Usage

```javascript
var script = document.createElement('script'); 
script.src = 'http://server.example.com/Users/1234?callback=parseResponse';
document.getElementsByTagName('head')[0].appendChild(script); 

function parseResponse(data){ 
  //callback method 
}
```

```javascript
$.ajax({
  url: 'http://server.example.com/Users/1234',
  dataType: 'jsonp',
  jsonpCallback: "parseResponse",
  success: callback
});
```
