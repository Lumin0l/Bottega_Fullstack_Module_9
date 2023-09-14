# Special Properties for the infinite scroll: innerHeight, scrollTop, offsetHeight

They are **vanilla JS properties**, can be used in any app.

## innerHeight

Tracks the **viewport height (vh)** value.

## scrollTop

Gets or sets the number of px that an element's content is scrolled vertically. So, starting from the top (of the viewport), it will tell you how many pixels the user scrolled at any given moment.

## offsetHeight

How long the whole document is, all of it, not only vh.

---

Taking this data we can do: if (innerHeight + scrollTop === offsetHeight) { trigger event } -> Translation: if (vh + scroll poinnt === the whole lenght of screen) { trigger event }.
