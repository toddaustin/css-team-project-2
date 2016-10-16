#&lt;q&gt;
*the &lt;q&gt; tag represents the HTML quote element.*

The html element `<q>` is used for short, inline quotations. When modern browsers, other than Internet Explorer, encounter the `<q>` element, they will insert quotation marks around the content inbetween the `<q>` tags. For Internet Explorer you as the developer would have to add CSS styles to the element. For example, in modern browsers, the following should show quotes: <q>This is an example of the &lt;q&gt; element</q>

## Syntax

The syntax of the `<q>` element is as follows: It must have a start and an end tag, and as it is an inline element, it lives inside parent elements such as `<p>, <a>, and <div>`.
```
<p>In Star Wars, Han Solo says <q>I've got a bad feeling about this</q> before the walls of the trash compactor start to close in.</p>
```
The above will render in the browser as:
<p>In Star Wars, Han Solo says <q>I've got a bad feeling about this</q> before the walls of the trash compactor start to close in.</p>

### Attributes

The `<q>` element can contain the `cite` attribute. The cite attribute is used to reference the url from which the quotation is sourced from. The cite attribute can be used by screen readers, but currently no normal browser displays or uses the `cite` attribute.

```html
<p>In Star Wars, Han Solo says <q cite="http://www.starwars.com">I've got a bad feeling about this</q> before the walls of the trash compactor start to close in.</p>
```

## Special Notes

For larger quotes use `<blockquote>`.
