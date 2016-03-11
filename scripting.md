

Scripting
---------

### Omit `type` attribute for JavaScript

> Bad:

    <script type="text/javascript">
      ...
    </script>

Good:

    <script>
      ...
    </script>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

### Add `defer` attribute if `script` element has `async` attribute

> Bad:

    <script async src="/js/main.js"></script>

Good:

    <script async defer src="/js/main.js"></script>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

### Don't comment out contents of `script` element

> Bad:

    <script>
    /*<![CDATA[*/
      ...
    /*]]>*/
    </script>

Also > bad:

    <script>
    <!--
      ...
    // -->
    </script>

Good:

    <script>
      ...
    </script>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

### Don't use script-injected `script` element

> Bad:

    <script>
      var script = document.createElement('script');
      script.async = true;
      script.src = "//example.com/widget.js";
      document.getElementsByTagName('head')[0].appendChild(script);
    </script>

Good:

    <script async defer src="//example.com/widget.js"></script>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!
