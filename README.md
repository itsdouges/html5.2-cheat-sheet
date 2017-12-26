# HTML5.2 Cheat Sheet

This cheat sheet will primarily be going over sematic markup changes, and things that affect the average web app developer. For a full summary of HTML5.2 go check out the [w3 changes](https://www.w3.org/TR/html52/changes.html#changes).

## [<dialog>](https://www.w3.org/TR/html52/interactive-elements.html#elementdef-dialog)

Now there is semantic meaning when wanting a `dialog`.

```html
<dialog id="my-dialog" open>
    Hello, World!
</dialog>
```

* Note the use of the `open` attribute. It should only be shown to the user if it is present.
* Do not set tab index on a dialog.

### Programatic usage

```javascript
const dialog = document.getElementById("my-dialog");

// Displays the dialog element.
dialog.show(/* optional anchor element */);

// Displays the dialog element and makes it the top-most modal dialog.
dialog.showModal(/* optional anchor element */);

// Closes the dialog element.
dialog.close(/* optional return value */ "my-value");

// Returns the dialog’s return value.
dialog.returnValue; // 'my-value'
```

## New markup constructions

* `<style>` can be placed within `<body>` now.
* Multiple `<main>` can exist, _so that only one is visible to the user_.
* `<div>` as a child of a `<dl>` element.
* `<dfn>` as a descendent of an `<li>` element that contains a definition of the term defined.
* Headings within `<legend>` in a `<fieldset>`.
* Empty `<option>` element as a child of `<datalist>`.

## Invalid constructions

* `roles` value for `<caption>` element
* Inline blocks/tables/floats/positioned block-level elements inside a `<p>`.
