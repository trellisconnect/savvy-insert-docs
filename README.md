# Savvy Insert

Savvy Insert allows users to quickly and easily find savings on their existing insurance.

Your website or mobile app can easily embed a prompt to find savings without navigating off your property.

<div style="max-width: 450px;margin:0 auto;">
![""](/screenshot.png?raw=true)
</div>

## Basic Usage

```html
<html>
  <head>
    <title>Example HTML Page</title>
    <!-- Add the Savvy Insert script tag-->
    <script src="https://cdn.savvy.insure/insert/v1.0/savvy-insert.js"></script>
  </head>
  <body>
    <!-- Add the Savvy Insert element where you would like the widget to display in your page -->
    <ins
      class="savvyinsert"
      data-url-tracking-params="REPLACE-THIS-WITH-STRING-FROM-SAVVY"
      style="display:inline-block;width:608px;height:329px;"
    ></ins>
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

## Design Considerations

The Savvy Insert is designed to be responsive by default and should "just work" in your primary content area. In order to display optimally it should be at least 300px wide.
