# supertoggle
A jquery "super toggle" for declaratively toggling anything on or off.

Setting things up is as easy as declaring your intent.

```html
<!-- For example: -->
<a href="#" data-swap='{
    "#swappable-1": [{".btn-success": ".btn.btn-sm.btn-default"}],
    "#swappable-1 .leftarr": [{"": ".hidden"}],
    "#swappable-1 .rightarr": [{".hidden": ""}],

    "#left-panel": [{"": ".hidden-lg"}],
    "#main-col": [{".col-lg-9.col-md-9": ".col-lg-12.col-md-12"}]
}'>Click me!</a>
```

### Initialize
* Add the script to your document, after jQuery.
* Initialize whatever selector you want. E.g. ```$('[data-toggle="swappable"]').on('click', supertoggle);```

### Declare
Elements must have ```data-toggle="swappable"``` set, and declarations are done via ```data-swap='{"#selector": [{".from1": ".to1"}, {".from2": ".to2"}]}'``` Where each <strong>key</strong> is a jquery selector, and each <strong>value</strong> is an <strong>array of objects with one key and one value</strong>, describing the swap <strong>from</strong>, and swap <strong>to</strong> values. There's no limit to how many you can use.
### More advanced usage
See the above examples for multiple selectors, pseudo-selectors and more.

Check out the [demos page](http://christabor.github.io/supertoggle/) for more examples!
