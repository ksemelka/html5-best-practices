# Markup Style

> By defining a strict syntax for your code, you create consistency for you and for people reading your code.

## Table of Contents

1. [Markup Syntax](#markup-syntax)
2. [Closing Elements](#closing-elements)
3. [Attributes](#attributes)
4. [Attributes](#attributes)

## Markup Syntax

### Always lowercase your markup syntax

> **[?]** There is no need to UPPERCASE your markup syntax. Despite of also being valid in HTML5, it difficults code readability and offers little help if the plan is to separate markup from content. For that purpose, you can always change your text editor theme.

Bad:

```html
<ARTICLE>
    <HEADER>
        <H1>Spanish Castle Magic</H1>
    </HEADER>
    ...
</ARTICLE>
```

Good:

```html
<article>
    <header>
        <h1>Spanish Castle Magic</h1>
    </header>
    ...
</article>
```

## Closing Elements

### Always close elements with its ending-tag

> **[?]** Browsers will try to automatically close elements that contain ending-tags. knowing where a `<div>` ends makes a clearer code, and doing this consistently enhances clarity and makes your code easier to maintain.

Bad:

```html
<article>
    <header>
        <h1>If 6 was 9
        ...
    <footer>by Jimi Hendrix
```

Good:

```html
<article>
    <header>
        <h1>If 6 was 9</h1>
    </header>
    ...
    <footer>
        by Jimi Hendrix
    </footer>
</article>
```

### Don't self-close elements with slash `/` for elements with no ending-tag

> **[?]** Self-closed elements (also called *void elements*) don't need a slash `/` to close itself. 
> [From W3C](https://www.w3.org/TR/html-markup/syntax.html): *"Void elements only have a start tag; end tags must not be specified for void elements".*

Bad:

```html
<img src="jimi-hendrix.jpg" alt="Jimi Hendrix drinking coffee"/>
```

Good:

```html
<img src="jimi-hendrix.jpg" alt="Jimi Hendrix drinking coffee">
```

## Attributes

### Attribute Order

> **[?]** Ordering attributes in the same manner creates a eye pattern and ease your code's readability.

1. `id`
2. `name` (if applicable)
3. `class`
4. ``src`, `for`, `type`, `href`, `value`
5. `title`, `alt`
6. `data-*`
7. `role`, `aria-*`

`Id`s are unique for each element, and should come first to make it easier to anchor a link or call it via script. `Class`es comes after, since almost every element has one. Atrributes like `src`, `for`, `type`, `href` and `value`, exposes information about the element's function and should also be immediately exposed in a first view. Elements like `title`, `alt`, `data-*`, `role` and `aria-*`, which are not so common in all elements, should come after.

**_Notice that it's a personal pattern with justified usage, and so it has no *bad practice*. Feel free to use or ignore it._**

### Always use quotes for attributes

> **[?]** Despite values with spaces or some non-alphanumeric characters, you can omit quotes for attribute values, and still have a valid HTML5 document, but **this approach not only makes your code inconsistent and harder to read**, but also **makes it harder to be compatibible with older browsers**. So, **always** use quotes for attributes.

Bad:
```html
<a href=about-hendrix.html>About Jimi Hendrix</a>
```

Good:

```html
<a href="about-hendrix.html">About Jimi Hendrix</a>
```
