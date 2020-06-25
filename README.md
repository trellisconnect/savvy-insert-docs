# Savvy Insert

Savvy Insert allows users to quickly and easily find savings on their existing insurance.

Your website or mobile app can easily embed the "Savvy Insert" so that users can find these savings without ever navigating off your property.

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
      data-savvy-insert
      data-urlTrackingParams="REPLACE-THIS-WITH-STRING-FROM-SAVVY"
    ></ins>
  </body>
</html>
```

## Advanced Usage

Adding your Trellis Client ID as a data parameter will brand the insert and modal widget with your name and logo. It will also enable you to access your users' information via Trellis API.

```html
    <ins
      data-savvy-insert
      data-urlTrackingParams="REPLACE-THIS-WITH-STRING-FROM-SAVVY"
      data-trellisClientId="YOUR-TRELLIS-CLIENT-ID"
    ></ins>
```
