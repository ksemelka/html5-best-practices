# Scripting

> Scripts allow authors to add interactivity to their documents.

## Prefer Progressive Enhancement over Graceful Degradation

Progressive Enchancement means that your site works perfectly without JavaScript enabled, and is enhanced progressively with JS to improve user experience. For warning messages, use the `<noscript>` tag.

> Bad:

```html
<noscript>
    This site requires JavaScript enabled. 
    Please enable it to see its content.
</noscript>
```

> Good:

A fully functional website not JavaScript dependent. 

```html
<noscript>
    You're experiencing this website without JavaScript enabled. 
    To enhance your experience, please enable it.
</noscript>
```

> Why?

Sites relying on Graceful Degradation are built on top of JS, usually warning the user that the site won't works well without it and offering little or none funcionalities for disabled JS clients. By choosing Progressive Enhancement you ensure that, despite the lack of JS, your website doesn't break user experience. 


## Use `async` attribute for non-blocking `script`s

For scripts that doesn't interfer on page's rendering, use `async`. A classical example would be Google Analytics code.

> Bad:

```html
<script src="//www.google-analytics.com/analytics.js"></script>
```

> Good:

```html
<script async src="//www.google-analytics.com/analytics.js"></script>
```

> Why?

The `async` attribute downloads a script without blocking the rest of the page loading. By declaring it, HTML parsing may continue and the script will be executed as soon as it’s ready.


### Omit `type` attribute for JavaScript

> Bad:

```html
<script type="text/javascript" src="voodoo-child.js"></script>
```

> Good:

```html
<script src="voodoo-child.js"></script>
```

> Why?

Since the creation of HTML5 doctype, the `type` attribute is no longer required. By omitting it, browsers implicitely undestands it as `text/javascript`.


## Avoid the use of inline scripts

> Bad:

``` js
<script>
    (function(){
        console.log('Highway Chile');
    })();
</script>
```

> Good:

```html
<script src="highway-chile.js"></script>
```

> Why?

HTML files should, ideally, contain only the presentation layer (the View), keeping it separated from the Controller (JavaScript). This concept if often called *Separation of Concern*. Separate HTML from JS makes it easier for you (and people dealing with your code) to read and maintain both the visual and functional aspects.
