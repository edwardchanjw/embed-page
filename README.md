# \<embed-page/\>
Proof of concept for Embeddable Progressive Application - WebComponent acting as IFRAME.

The scope insulation for DOM and CSS is done by WebComponet shadow dom, API for JS 
are insulated by closure for global objects with wrappers limiting the dom access root 
to component content. Similar approach will be applied for url, storage, cookies, etc. 


## To see in action 
Run
```
$ polymer serve --open
```
Which will open the demo page in browser. 
There the external page is loaded into shadow dom and its embedded and referenced JS
will work with document via wrapper in same way as standalone page. 

The host page document is not available from embedded content. 


## Preparing project
```
$ bower install
```
## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. 
Then run `polymer serve --open` to serve your element locally.



## Running Tests

```
$ polymer test
```

Application is set up to be tested via 
[web-component-tester](https://github.com/Polymer/web-component-tester). 
Run `polymer test` to run your application's test suite locally.