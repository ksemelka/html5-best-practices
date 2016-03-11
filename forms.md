# Forms

> Description here

## Wrap form control with `label` element

> Bad:

    <p>Query: <input name="q" type="text"></p>

> Good:

    <p><label>Query: <input name="q" type="text"></label></p>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Use appropriate `type` attribute for `input` element

> Bad:

    <label>Search keyword: <input name="q" type="text"></label>

> Good:

    <label>Search keyword: <input name="q" type="search"></label>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Add `value` attribute to `input type="submit"`

> Bad:

    <input type="submit">

> Good:

    <input type="submit" value="Search">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Add `title` attibute to `input` element when there is `pattern` attribute

> Bad:

    <input name="security-code" pattern="[0-9]{3}" type="text">

> Good:

    <input name="security-code" pattern="[0-9]{3}" title="A security code is a number in three figures." type="text">

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Don't use `placeholder` attribute for labeling

> Bad:

    <input name="email" placeholder="Email" type="text">

> Good:

    <label>Email: <input name="email" placeholder="john.doe@example.com" type="text"></label>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Add `max` attribute to `progress` element

> Bad:

    <progress value="0.5"> 50%</progress>

> Good:

    <progress max="100" value="50"> 50%</progress>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Add `min` and `max` attribute to `meter` element

> Bad:

    <meter value="0.5"> 512GB used (1024GB total)</meter>

> Good:

    <meter min="0" max="1024" value="512"> 512GB used (1024GB total)</meter>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!


## Place `legend` element as first child of `fieldset` element

> Bad:

    <fieldset>
      <p><label>Is this section is useful?: <input name="usefulness-general" type="checkbox"></label></p>
      ...
      <legend>About "General"</legend>
    </fieldset>

> Good:

    <fieldset>
      <legend>About "General"</legend>
      <p><label>Is this section is useful?: <input name="usefulness-general" type="checkbox"></label></p>
      ...
    </fieldset>

> Why?

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora dolorem hic soluta labore ad, temporibus inventore, omnis eius harum iste nobis dolore facere, ipsa quisquam expedita, officiis magnam. Voluptatem!