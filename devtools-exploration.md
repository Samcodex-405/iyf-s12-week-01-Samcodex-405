# DevTools Exploration

## Website 1: Example.com

**Website:** https://example.com

### 1. What HTML tags are used on the page?

The visible HTML tags include:

- `<html>`
- `<head>`
- `<meta>`
- `<link>`
- `<title>`
- `<style>`
- `<body>`
- `<svg>`
- `<p>`
- `<a>`
- `<script>`

### 2. What is the page title?

The page title is **Example Domain**, as shown inside the `<title>` tag.

### 3. How many headings are there?

There are **0 headings** visible in the HTML structure. There are no heading tags such as `<h1>`, `<h2>`, or `<h3>` shown in the page structure.

---

## Website 2: MDN Web Docs

**Website:** https://developer.mozilla.org

### 1. Find the navigation menu - what tag is it wrapped in?

The navigation menu is wrapped in a `<nav>` element:

`<nav class="navigation" data-scheme="dark" data-open="false">`

It sits inside `<header class="page-layout__header">` and is laid out using CSS Grid.

Its children include:

- `div.navigation__logo` - contains the MDN logo.
- `div.navigation__search` - contains the search area.
- `button.navigation__button` - the hamburger navigation toggle, with `aria-label="Toggle navigation"` and `aria-expanded="false"`.
- `div.navigation__popup#navigation__popup` - contains the menu that opens when the navigation toggle is activated.

### 2. How is the search bar structured?

The search area is built using custom web components rather than being a simple `<input>` directly inside the navigation.

The mobile search area contains:

`<div class="navigation__search" data-view="mobile">`

Inside it is the custom `<mdn-search-button>` element.

The `<mdn-search-button>` has an open `#shadow-root`, which means its internal HTML is encapsulated inside the Shadow DOM.

There is also a separate `<mdn-search-modal id="mdn-search">` element inside the header. This provides the full search overlay that opens when the search button is clicked.

Therefore, the search structure consists of a search button that triggers a search modal.

### 3. What happens when you hover over links?

The links in the hero section (**CSS**, **HTML** and **JavaScript**) are underlined by default. The rule `.homepage-hero a` in `server.css` sets:

```css
.homepage-hero a {
  color: var(--color-link-normal);
  text-decoration: underline;
}
```

When a link is hovered over or focused, the rule `:is(.homepage-hero a):hover` (also in `server.css`) applies:

```css
:is(.homepage-hero a):focus, :is(.homepage-hero a):hover {
  text-decoration: none;
}
```

Therefore, when the user hovers over a link, the **underline disappears**.

The link colour stays the same, and the cursor changes to a pointer through the browser's default link styling (`cursor: pointer`).

---

## Website 3: W3Schools

**Website:** https://www.w3schools.com/html/default.asp

### 1. Identify 5 different HTML elements

The following HTML elements were identified:

1. `<div>` - used as a container for content.
2. `<p>` - used for paragraphs of text.
3. `<hr>` - creates a horizontal rule separating content.
4. `<h2>` - represents a second-level heading.
5. `<form>` - contains form controls used to submit information.

Other elements identified during the inspection included:

- `<input>`
- `<label>`
- `<button>`
- `<br>`

### 2. Find a form element and list its inputs

The inspected form was:

`<form action="exercise.asp?x=xrcise_links1" method="post" rel="noopener">`

Inside the form, I identified radio button inputs:

`<input type="radio" name="quizoption" id="quizoption0">`

and:

`<input type="radio" name="quizoption" id="quizoption2">`

The form also contains labels associated with the radio buttons and a submit button:

`<button type="submit" class="ws-btn">Submit Answer</button>`

### 3. Screenshot of the Elements panel

A screenshot was taken while inspecting the W3Schools Elements panel.

The screenshot shows the expanded `<form>` element, the radio button inputs, their associated labels, and the submit button.

---

## Conclusion

Using browser DevTools, I inspected the HTML structure, navigation, search interface, CSS hover behavior, forms, inputs, and other HTML elements on three different websites.

This exercise helped me understand how HTML elements and CSS styles are structured and how browser DevTools can be used to inspect and understand webpages.