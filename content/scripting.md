# Scripting

> Scripts allow authors to add interactivity to their documents.

## Table of Contents

1. [Development Approaches](#development-approaches)
2. [Separation of Concerns](#separation-of-concerns)
3. [Async Attribute](#async-attribute)
4. [Type Attribute](#type-attribute)

## Development Approaches

### Prefer Progressive Enhancement over Graceful Degradation

> **[?]** Sites relying on Graceful Degradation are built on top of JS, offering little or no funcionalities for disabled JS clients. Prefer Progressive Enhancement to ensure that, despite the lack of JS, your website doesn't break user's experience.

```html
<!-- Bad -->
<noscript>
This site requires JavaScript enabled.
Please enable it to see its content.
</noscript>

<!-- Good -->
<!-- A fully functional website not JavaScript dependent. -->
<noscript>
You're experiencing this website without JavaScript enabled.
To enhance your experience, please enable it.
</noscript>
```

## Separation of Concerns

### Avoid the use of inline scripts

> **[?]** HTML files should contain only the presentation layer (the View), keeping it separated from the Controller (JavaScript). This concept is called *Separation of Concerns*. Separated files are easier to maintain both visually and functionally.

``` html
<!-- bad -->
<script>
(function(){
console.log('Highway Chile');
})();
</script>

<!-- Good -->
<script src="highway-chile.js"></script>
```

## Async Attribute

### Use `async` attribute for non-blocking `script`s

> **[?]** The `async` attribute downloads a script without blocking the rest of the page loading. By declaring it, HTML parsing may continue and the script will be executed as soon as it’s ready.

```html
<!-- Bad -->
<script src="//www.google-analytics.com/analytics.js"></script>

<!-- Good -->
<script async src="//www.google-analytics.com/analytics.js"></script>
 ```

## Type Attribute

### Omit `type` attribute for JavaScript

> **[?]** Since the creation of HTML5 doctype, the `type` attribute is no longer required. By omitting it, browsers implicitely undestands it as `text/javascript`.

```html
<!-- bad -->
<script type="text/javascript" src="voodoo-child.js"></script>

<!-- good -->
<script src="voodoo-child.js"></script>
```
