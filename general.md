# General

> Description

## Start with DOCTYPE

> Bad:

    <html>
      ...
    </html>

> Good:

    <!DOCTYPE html>
    <html>
      ...
    </html>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't use character references as much as possible

> Bad:

    <p><small>Copyright &copy; 2014 W3C<sup>&reg;</sup></small></p>

> Good:

    <p><small>Copyright © 2014 W3C<sup>®</sup></small></p>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Escape `&`, `<`, `>`, `"`, and `'` with named character references

> Bad:

    <h1>The "&" character</h1>

> Good:

    <h1>The &quot;&amp;&quot; character</h1>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Put white spaces around comment contents

> Bad:

    <!--This section is non-normative-->

> Good:

    <!-- This section is non-normative -->

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't mix empty element format

> Bad:

    <img alt="HTML Best Practices" src="/img/logo.png">
    <hr />

> Good:

    <img alt="HTML Best Practices" src="/img/logo.png">
    <hr>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't put white spaces around tags and attribute values

> Bad:

    <h1 class=" title " >HTML Best Practices</h1>

> Good:

    <h1 class="title">HTML Best Practices</h1>


## Don't mix character cases

> Bad:

    <a HREF="#general">General</A>

> Good:

    <a href="#general">General</a>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't mix quotation marks

> Bad:

    <img alt="HTML Best Practices" src='/img/logo.jpg'>

> Good:

    <img alt="HTML Best Practices" src="/img/logo.jpg">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't separate attributes with two or more white spaces

> Bad:

    <input   name="q"  type="search">

> Good:

    <input name="q" type="search">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Omit boolean attribute value

> Bad:

    <audio autoplay="autoplay" src="/audio/theme.mp3">

> Good:

    <audio autoplay src="/audio/theme.mp3">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Omit namespaces

> Bad:

    <svg xmlns="http://www.w3.org/2000/svg" version="1.1">
      ...
    </svg>

> Good:

    <svg version="1.1">
      ...
    </svg>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't mix `data-*`, Microdata, and RDFa Lite attributes with common attributes

> Bad:

    <img alt="HTML Best Practices" data-height="31" data-width="88" itemprop="image" src="/img/logo.png">

> Good:

    <img alt="HTML Best Practices" src="/img/logo.png" data-width="88" data-height="31" itemprop="image">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Prefer strong native semantics

> Bad:

    <nav role="navigation">
      ...
    </nav>
    
    <hr role="separator">

> Good:

    <nav>
      ...
    </nav>
    
    <hr>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!