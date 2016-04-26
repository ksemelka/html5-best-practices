# Document Metadata

> Metadata is the information that documents provides to browsers concerning to how it's going to be presented and its behaviour. It could also (if applicable), provide information about its relationship with other documents.

## Table of Contents

1. [Head](#head)
2. [Title](#title)
3. [Base](#base)
4. [Link](#link)
5. [Style](#style)
6. [Meta](#meta)

> **[!]** For best practices related to `<noscript>` and `<script>` elements, go to [Scripting](scripting.md) section.

## Head

### Follow this priority order for metadata elements inside the `<head>` element

> **[?]** Browsers only sniff a limited number of bytes (512) at the beginning to read things like content type and character encoding. By following the pattern below you avoid any errors related to browser rendering:

1. `<meta charset="utf-8">`
1. `<meta http-equiv="X-UA-Compatible" content="IE=edge">` (if applicable)
3. `<meta name="viewport" content="width=device-width, initial-scale=1">` (if applicable)
3. `<base>` (if applicable)
4. `<title>...</title>`
5. Other stuff: other `<meta>` (`author`, `name`, `description`), `<link>`, `<style>`, etc.

## Title

### For SEO purposes, avoid making your `<title>` longer than 55~57 characters

> **[?]** The title element is the most important element related to SEO. It's usually used as a title for Search Engines result pages (SERP), as a tab title for browsers, and as a title for social sharing. By making it approximately 55 character longer max, you increase the chances of it being displayed properly on these medias.

Bad:

```html
<head>
    <title>Several Species Of Small Furry Animals Gathered Together in A Cave And Grooving With A Pict</title>
    ...
</head>
```

Good:

```html
<head>
    <title>Several Species Of Small Furry Animals Gathered Together</title>
    ...
</head>
```

### For SEO purposes, avoid repeating the same text for `<title>` and `<h1>` elements

> **[?]** The content inside an `<h1>` element also represents the main theme of a page (as `<title>` does), but for Search engines it would be placed inside the description box. By repeating the same content of your `<title>`, you lose the oportunity to increase relevant information on a SERP.

Bad:

```html
<head>
    <title>Houses of the Holy</title>
</head>
<body>
    <h1>Houses of the Holy</h1>
</body>
```

Good:

```html
<head>
    <title>Houses of the Holy</title>
</head>
<body>
    <h1>Houses of the Holy is the fifth studio album by English rock band Led Zeppelin, released by Atlantic Records on 28 March 1973. It is their first album composed of entirely original material.</h1>
</body>
```

### For SEO purposes, avoid the use of your brand's name or make the it last text inside `<title>` element

> **[?]** The `<title>` element has an descending value of keyword relevance. It means that Search Engines will make it more relevant for keywords that it founds first. By omitting your brand's name or making it as the last string of your title, you increase the chances of important keywords to being found.

Bad:

```html
<head>
    <title>Pink Floyd - A Momentary Lapse of Reason</title>
</head>
```

Good:

```html
<head>
    <title>A Momentary Lapse of Reason - Pink Floyd</title>
</head>
```

## Base

### If you have full control over your application links, use the `<base>` element to define your default link targets

> **[?]** By setting your `<base>` element the `target` attribute, you define the base target of all your links inside your application.

Bad: 
```html
<body>
    <a href="link1.html" target="_blank">Link 1</a>
    <a href="link2.html" target="_blank">Link 2</a>
    <a href="link3.html" target="_blank">Link 3</a>
    <a href="link4.html" target="_blank">Link 4</a>
</body>
```

Good:

```html
<head>
    <base target="_blank">
</head>
<body>
    <!-- notice that all links below will behave like _blank was defined individually -->
    <a href="link1.html">Link 1</a>
    <a href="link2.html">Link 2</a>
    <a href="link3.html">Link 3</a>
    <a href="link4.html">Link 4</a>
</body>
```

### Declare the `<base>` element only once per page

> **[?]** The `<base>` element accepts only two attributes: `href` and `target`. Despite being possible, and semanticaly correct to have both declared (only if their attributes differ from each other). You should, for consistency and readability, declare them together.

Bad:

```html
<head>
    <base href="http://ledzeppelin.com/app/">
    <base target="_blank">
</head>
```

Good:

```html
<head>
    <base href="http://ledzeppelin.com/app/" target="_blank">
</head>
```

### Use the `<base>` as one of the top elements inside the `<head>` element

> **[?]** Since the `<base>` purpose is to serve as a base for relative URLs. Include it as one of the top elements of your application. Preferably the first one after `charset`, `http-equiv` and `viewport` meta attributes.

Bad:

```html
<head>
    <meta charset="utf-8">
    <meta name="author" content="awesome community">
    <meta name="description" content="html5 best practices...">
    <title>HTML5 Best Practices</title>
    <base target="_self"></base><!-- I'm the last :'( -->
</head>
```

Good:

```html
<head>
    <meta charset="utf-8">
    <base target="_self"></base><!-- I'm here now!! Cool. -->
    <title>HTML5 Best Practices</title>
    <meta name="author" content="awesome community">
    <meta name="description" content="html5 best practices...">
</head>

```

## Style

### Only use `<style>` to inline critical CSS

> **[?]** Following the [Separation of Concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) principle, and applying to Web Development, styles should have it own separated file. However, the Critical CSS approach is a technique to speed up the rendering of an application. The *critical* part stands for the part that user can see when they first load the page. If you go to any page, the content you see before you scroll can be considerated *critical*. For those, apply the `<style>` element to inline your critical CSS.

Bad:

```html
<head>
    ...
    <style>
        /* Hey! Your website footer is not critical! */
        body > footer {
            color: white;
            background-color: black;
        }
    </style>
</head>
```

Good:

```html
<head>
    ...
    <style>
        /* Users see it first? Critical! Style to the rescue */
        header[role="banner"] {
            color: white;
            background-color: black;
        }
    </style>
</head>
```

## Link

### Omit the `type` attribute for `<link>` elements

> **[?]** According to the [specification](http://www.w3.org/TR/html5/links.html#link-type-stylesheet), the default type for resources given by the `stylesheet` keyword is `text/css`.

Bad:

```html
<head>
    ...
    <link href="file.css" rel="stylesheet">
</head>
```

Good:

```html
<head>
    ...
    <link href="file.css">`
</head>
```

## Meta

### Minimize XSS risks by declaring `<meta>` charset attribute with `UTF-8`

> **[?]** Cross Site Scripting (XSS) allows the injection of malicious scripts inside a document. Historicaly, the UTF-7 encoding allows the rendering of opening tags with `+ADw-` and closing tags with `+AD4-`, making it open for script injection. By setting your charset to UTF-8, you can minimize the risk of XSS attacks.

Bad:

```html
<head>
    <!-- no meta charset here -->
    <title>Black Night</title>
</head>
```

Good:

```html
<head>
    <meta charset="utf-8">
    <title>Black Night</title>
</head>
```

**Note:** If you like futher information about XSS, [this page](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet) explains awesome practices to bulletproof your application.

### Declare your `Viewport` meta tag with `width=device-width` and `initial-scale=1"` as its content

> **[?]** Setting your document width relative to the device-width and by setting the scale default to 1, you avoid some devices from zooming your document in a landscape view, making your application consise and optimized for mobile devices.

Bad:

```html
<head>
    ...
    <meta name="viewport" content="width=320, initial-scale=1">
</head>
```

Good:

```html
<head>
    ...
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
```


### Don't set `minimum-scale`, `maximum-scale` and `user-scalable` values for the `Viewport` meta tag

> **[?]** By setting a minimum, maximum and removing the user's option to scale the document, you compromise acessibility, since you can't control if users are seeing your content properly.

Bad:

```html
<head>
    ...
    <meta name="viewport" content="width=device-width, maximum-scale=1.0, user-scalable=no">
</head>
```

Good:

```html
<head>
    ...
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
```
### For better legacy browser rendering, declare the pragma directive `X-UA compatible` with `content="IE=Edge"`

> **[?]** By declaring `X-UA compatible`, you force old IE versions to render pages acconding with the rendering of the latest IE version. Despite all discussion evolving this pragma directive, this practice has proven to be the most reliable and is used by heavy community-driven projects, such as [Twitter Bootstrap](https://github.com/twbs/bootstrap/blob/master/docs/examples/starter-template/index.html) and [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate/blob/master/src/index.html).

Bad:

```html
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```

Good:

```html
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```

### For a better SEO, always declare `author` and `description` metadata

> **[?]** Since the `keyword` metadata is almost ignored by search engines due to its historical abuse by authors, declaring `author` and `description` with strong keywords related to your page content, you increase the chance to appear higher in search results.

Good:

```html
<meta name="author" content="HTML5 Best Practices community">
<meta name="description" content="A collection of Community's acclaimed best practices, advices and notes for writing scalable and sustainable HTML5 documents. Enforces semantic principles with short explanations about the most common elements of an HTML5 Application.">
```

### If you're building a Web Application instead of a Web Site, declare the `application-name` metadata

> **[?]** Browsers may prefer the `application-name` metadata over the `<title>` element to represent the application name for a better UI, due to the common application nature that may include status messages and other dynamic information.

Good:

```html
<meta name="application-name" content="App Name">
```
