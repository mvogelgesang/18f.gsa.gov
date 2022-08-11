---
title: Inline frames (iframes)
lead: 'How we deal with iframes'
permalink: /guides/accessibility/iframes/
agency: iframes
subnav_title: Inline Frames
subnav_items:
  - text: Testing
    permalink: /guides/accessibility/iframes/#testing
  - text: Examples
    permalink: /guides/accessibility/iframes/#examples

---
When using `iframe`s, it’s important that all content contained in them is accessible.

## Testing

1. Identify all `iframe`s on a page.
2. Using the keyboard, navigate to each `iframe` to ensure content is accessible.
3. Check the `title` or `name` attribute of each `iframe` for a description of the content.

## Examples


### Failures

<iframe src="../iframeform/" class="exampleFailure"></iframe>

```html
<iframe src="../iframeform/"></iframe>
```

> This `iframe` doesn’t have a `title` or `name`.

<iframe src="../iframeform/" name='Provide an address form' class="exampleFailure"></iframe>

```html
<iframe src="../iframeform/" name='Provide an address form'></iframe>
```

> This `name` isn’t correct.

### Passes

<iframe src="../iframeform/" title='Provide Name Form'></iframe>

```html
<iframe src="../iframeform/" title='Provide Name Form'></iframe>
```

> Correct `title` is provided. This would also pass if this information was in a `name` attribute.

