## Older syntaxes for event handling

In addition to the recommended modern addEventListener method discussed in the main material, two older syntaxes exists
for event handling.

### Old (90s)

Inline syntax where the event handler is specified in the HTML code. This method should be avoided. Admittedly, some
frameworks and libraries, such as Angular and React, use a syntax like this, but they are special cases.

```html

<button onclick="popup()">Click me</button>
<script>
    function popup(evt) {
        alert('Element' + evt.currentTarget + ' was clicked');
    }
</script> 
```

### Traditional (2000s)

[Onevent properties](https://developer.mozilla.org/en-US/docs/Web/Events/Event_handlers#using_onevent_properties) are a
handy way to do transaction processing. They are recommended for use only in the simplest applications.

```html

<button>Click me</button>
<script>
    const button = document.querySelector('button');

    function popup(evt) {
        alert('Element' + evt.currentTarget + ' was clicked');
    }

    button.onclick = popup;
</script>
```


