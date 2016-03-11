# Embedded content

## Add `alt` attrbute to `img` element if needed

> Bad:

    <img src="/img/logo.png">

> Good:

    <img alt="HTML Best Practices" src="/img/logo.png">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!

## Provide fallback content for `audio` or `video` element

> Bad:

    <video>
      <source src="/mov/theme.mp4" type="video/mp4">
      <source src="/mov/theme.ogv" type="video/ogg">
      ...
    </video>

> Good:

    <video>
      <source src="/mov/theme.mp4" type="video/mp4">
      <source src="/mov/theme.ogv" type="video/ogg">
      ...
      <iframe src="//www.youtube.com/embed/..." allowfullscreen></iframe>
    </video>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!