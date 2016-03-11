# Text-level semantics

> Description

## Don't split same link that can be grouped

> Bad:

    <h1><a href="https://whatwg.org/">WHATWG</a></h1>
    
    <p><a href="https://whatwg.org/">A community maintaining and evolving HTML since 2004.</a></p>

> Good:

    <a href="https://whatwg.org/">
      <h1>WHATWG</h1>
    
      <p>A community maintaining and evolving HTML since 2004.</p>
    </a>


## Use `download` attribute for downloading a resource

> Bad:

    <a href="/downloads/offline.zip">offline version</a>

> Good:

    <a download href="/downloads/offline.zip">offline version</a>


## Use `rel`, `hreflang`, and `type` attribute if needed

> Bad:

    <a href="/ja/pdf">Japanese PDF version</a>

> Good:

    <a href="/ja/pdf" hreflang="ja" rel="alternate" type="application/pdf">Japanese PDF version</a>


## Clear link text

> Bad:

    <p><a href="/pdf" rel="alternate" type="application/pdf">Click here</a> to view PDF version.</p>

> Good:

    <p><a href="/pdf" rel="alternate" type="application/pdf">PDF version</a> is also available.</p>


## Don't use `em` element for warning or caution

> Bad:

    <em>Caution!</em>

> Good:

    <strong>Caution!</strong>


## Avoid `s`, `i`, `b`, and `u` element as much as possible

> Bad:

    <i class="icon-search"></i>

> Good:

    <span class="icon-search" aria-hidden="true"></span>


## Don't put quotes to `q` element

> Bad:

    <q>“For writing maintainable and scalable HTML documents”</q>

> Good:

    <q>For writing maintainable and scalable HTML documents</q>

Also > good:

    “For writing maintainable and scalable HTML documents”


## Add `title` attribute to `abbr` element

> Bad:

    <abbr>HBP</abbr>

> Good:

    <abbr title="HTML Best Practices">HBP</abbr>


## Markup `ruby` element verbosely

> Bad:

    <ruby>HTML<rt>えいちてぃーえむえる</ruby>

> Good:

    <ruby>HTML<rp> (</rp><rt>えいちてぃーえむえる</rt><rp>) </rp></ruby>


## Add `datetime` attribute to non-machine-readable `time` element

> Bad:

    <time>Dec 19, 2014</time>

> Good:

    <time datetime="2014-12-19">Dec 19, 2014</time>


## Specify code language with `class` attribute prefixed with `language-`

> Bad:

    <code>&lt;DOCTYPE html></code>

> Good:

    <code class="language-html">&lt;DOCTYPE html></code>


## Keep `kbd` element as simple as possible

> Bad:

    <kbd><kbd>Ctrl</kbd>+<kbd>F5</kbd></kbd>

> Good:

    <kbd>Ctrl+F5</kbd>


## Avoid `span` element as much as possible

> Bad:

    HTML <span class="best">Best</span> Practices

> Good:

    HTML <em>Best</em> Practices

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Break after `br` element

> Bad:

    <p>HTML<br>Best<br>Practices</p>

> Good:

    <p>HTML<br>
    Best<br>
    Practices</p>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Don't use `br` element only for presentational purpose

> Bad:

    <p><label>Rule name: <input name="rule-name" type="text"></label><br>
    <label>Rule description:<br>
    <textarea name="rule-description"></textarea></label></p>

> Good:

    <p><label>Rule name: <input name="rule-name" type="text"></label></p>
    <p><label>Rule description:<br>
    <textarea name="rule-description"></textarea></label></p>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!