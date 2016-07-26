##&lt;iron-url-history&gt;

`iron-url-history` is a Polymer element that allow storing navigation history while clicking in single page application.
This element share history between all the instances of the `iron-url-history` tag.
Can be imported in a custom element allowing to store navigation redirection ( like clicking and redirecting to the href on a `a` tag ).
`iron-url-history` store the navigation url, the date of redirection and, if present, a "user defined" additional paramenter. That will allow to
share additional information aboute navigation timeline.

The following methods are available for call:

| Method | Inputs | Outputs | Description |
| --- | --- | --- | --- |
| `goto` | url (string) | null | Simulate href redirection and store the url in navigation history |
| `pushLocation` | url (string), adds (object) | null | Push the url into navigation history and store additional user's defined information about that |
| `getCurrent` | null | { url (string), date (date), adds (object) } | Get the current view information |
| `getBack` | null | { url (string), date (date), adds (object) } | Get the previous view information |
| `getForward` | null | { url (string), date (date), adds (object) } | Get the previous view information |
| `getHistory` | null | [ { url (string), date (date), adds (object) } ] | Get the entire view history information |

To install the component with the Bower, just run: 

`bower install --save iron-url-history`

Example:

```html
<link rel="import" href="./iron-url-history.html">

<iron-url-history id="history" history={{history}}></iron-url-history>
```

An example on how to include the `iron-url-history` tag inside a custom link element is provided inside the `tag-a-history` tag ( also used inside the demo page ).

For a working sample about the `iron-url-history` tag check the [DEMO PAGE](http://alessiocarrafa.it/polymer-elements/iron-url-history/demo.html)