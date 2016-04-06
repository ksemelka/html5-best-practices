# Markup Style

> By defining a strict syntax for your code, you create consistency for you and for people reading your code.

## Always use quotes for attributes

> Bad:

```html
<a href=about-hendrix.html>About Jimi Hendrix</a>
```

> Good:

```html
<a href="about-hendrix.html">About Jimi Hendrix</a>
```

> Why?

Despite values with spaces or some non-alphanumeric characters, you can omit quotes for attribute values, and still have a valid HTML5 document, but **this approach not only makes your code inconsistent and harder to read**, but also **makes it harder to be compatibible with older browsers**. So, **always** use quotes for attributes.

## Always lowercase your markup syntax

> Bad:

```html
<ARTICLE>
    <HEADER>
        <H1>Spanish Castle Magic</H1>
    </HEADER>
    ...
</ARTICLE>
```

> Good:

```html
<article>
    <header>
        <h1>Spanish Castle Magic</h1>
    </header>
    ...
</article>
```

> Why?

There is no need to UPPERCASE your markup syntax. Despite of also being valid in HTML5, it difficult code readability and offers little help if the plan is to separate markup from content. For that purpose, you can always change your text editor theme.

## Always close elements with ending-tag

> Bad:

```html
<article>
    <header>
        <h1>If 6 was 9
        ...
    <footer>by Jimi Hendrix
```

> Good:

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

> Why?

Browsers will try to automatically close elements that contain ending-tags. knowing where a div ends just makes for clearer code, and doing this consistently enhances clarity and makes your code easier to maintain.

## Don't self-close elements with slash `/` for elements with no ending-tag

> Bad

```html
    <img src="jimi-hendrix.jpg" alt="Jimi Hendrix drinking coffee"/>
```

> Good

```html
    <img src="jimi-hendrix.jpg" alt="Jimi Hendrix drinking coffee">
```

> Why?

Self-closed elements (also called *void elements*) don't need a slash `/` to close itself. [From W3C](https://www.w3.org/TR/html-markup/syntax.html): *"Void elements only have a start tag; end tags must not be specified for void elements".*

## Attribute Order

> Notice that it's a personal pattern with justified usage, and so it has no *bad practice*. Feel free to use or ignore it.

To make it easier to read your code, your attributes should have the following order:

* `id`
* `name` (if applicable)
* `class`
* ``src`, `for`, `type`, `href`, `value`
* `title`, `alt`
* `data-*`
* `role`, `aria-*`

> Why?

Ordering attributes in the same manner creates a eye pattern and ease your code's readability.

`Id`s are unique for each element, and should come first to make it easier to anchor a link or call it via script. `Class`es comes after, since almost every element has one. Atrributes like `src`, `for`, `type`, `href` and `value`, exposes information about the element's function and should also be immediately exposed in a first view.

Elements like `title`, `alt`, `data-*`, `role` and `aria-*`, which are not so common in all elements, should come after.
