# bootstrap3-accessibility-patches

A package for making your bootstrap3 web app more accessible.
This Package tries to address accessibility related issues mostly related to keyboard navigation of your web-views.

  > 1. We start off making sure drop-downs and sub-menus get closed when they lose focus.
  > 2. We update area-expanded attributes accordingly when drop-downs are opened and closed.
  >      * Make sure you start off by adding are-expanded="false" to all .dropdown-toggle .trigger class elements.
  > 3. We automatically add attributes like role=menu to any .dropdown-menu or .dropdown-submenu menus. We also set aria-haspopup="true" and tabindex="0" on any a.trigger  a.dropdown-toggle links.
  > 3. We add the ability to open and close menus with the space-bar.
  > 4. We also prevent the enter key from submitting forms except when on the form submit button. When enter is pressed on
  >    a text input it will place focus on the next input. When it is pressed on a checkbox or radio button it will toggle
  >    the state of that input.
  > 5. Lastly, we make it easy to add a skip navigation link at the top of your page.

This Package depends on jQuery so you need to link to a version of jQuery that is greater than 1.9.1, but less than 2.0.0.
This package may work with older and or newer jquery versions than specified, but this is untested.

You will also need to link to index.js in this package.

```html
  <script src="node_modules/bootstrap3-accessibility-patches/index.js"></script>
  <script src="node_modules/jquery/dist/jquery.min.js">
```

## Creating a skip navigation link.

At the very top of the page you will need to create a link, That preferably, navigates to the first page heading after your navigation. This link needs to have an **ID** set to **skip-nav** like so.
```html
  <a link="#heading" id="skip-nav"><a>
```
And that's it, everything else happens behind the scenes.

## Disclaimer
This is not a solution to all your accessiblity woes, it's just a step in the right direction.
