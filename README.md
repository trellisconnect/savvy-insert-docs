# Savvy Insert

Savvy Insert allows users to quickly and easily find savings on their existing insurance.

Your website or mobile app can easily embed a prompt to find savings without navigating off your property.

![""](/insert-screenshot.png?raw=true)

## Basic Usage

```html
<html>
  <body>
    <!-- Add the Savvy Insert element where you would like the widget to display in your page -->
    <ins
      class="savvyinsert"
      data-url-tracking-params="REPLACE-THIS-WITH-STRING-FROM-SAVVY"
      style="display:inline-block;width:608px;height:329px;"
    ></ins>
    <!-- Add the Savvy Insert script tag-->
    <script
      src="https://cdn.savvy.insure/insert/v1.0/savvy-insert.js"
      async
    ></script>
  </body>
</html>
```

## Advanced Usage

Adding your Trellis Client ID as a data parameter will brand the insert and modal widget with your name and logo. It will also enable you to access your users' information via Trellis API.

```html
<ins
  class="savvyinsert"
  data-url-tracking-params="REPLACE-THIS-WITH-STRING-FROM-SAVVY"
  data-trellis-client-id="YOUR-TRELLIS-CLIENT-ID"
  style="display:inline-block;width:608px;height:329px;"
></ins>
```

## AMP Usage

The Savvy Insert relies on the `<amp-iframe>` element for AMP pages. [Read more](https://amp.dev/documentation/components/amp-iframe/).

```html
<!DOCTYPE html>
<html ⚡ lang="en">
  <head>
    <meta charset="utf-8" />
    <meta
      name="viewport"
      content="width=device-width,minimum-scale=1,initial-scale=1"
    />
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <!-- Load the AMP Iframe -->
    <script
      async
      custom-element="amp-iframe"
      src="https://cdn.ampproject.org/v0/amp-iframe-0.1.js"
    ></script>
    <link rel="canonical" href="..." />
  </head>
  <body>
    <!-- Load the Savvy Insert AMP page where you would like it to display -->
    <amp-iframe
      src="https://cdn.savvy.insure/insert/v1.0/amp.html"
      frameborder="0"
      data-url-tracking-params="YOUR_STRING_FROM_SAVVY"
      data-insert-theme="money"
      width="351"
      height="369"
      sandbox="allow-scripts allow-same-origin"
    >
      <amp-img
        layout="fill"
        src="https://via.placeholder.com/351x369"
        placeholder
      ></amp-img>
    </amp-iframe>
    <!-- -->
  </body>
</html>
```

## Design Considerations

The Savvy Insert has two sizes currently, 608 width x 392 height, and 345 width x 318 height. It will resize itself according to how much space is available for the insert.
