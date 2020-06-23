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
    <!-- Add the Savvy Insert div where you would like the widget to display in your page -->
    <div data-savvy-insert></div>

    <!-- Configure the Savvy Insert -->
    <script>
      SavvyInsert.configure({
        urlTrackingParams: 'REPLACE-THIS-WITH-STRING-FROM-SAVVY',
      });
    </script>
  </body>
</html>
```

## Advanced Usage

Full configuration options.

```html
<script>
  SavvyInsert.configure({
    urlTrackingParams: 'REPLACE-THIS-WITH-STRING-FROM-SAVVY',
    // OPTIONAL: Your Trellis Client ID. Required if you intend to collect end-user PII.
    trellisClientId: API_CLIENT_ID,

    // OPTIONAL: onConnect(connectionId, metadata)
    // Called when the user has authenticated access to their insurance account
    // and granted permission to Savvy to access its data.
    // - connectionId - Set to null if trellisClientId not provided.
    //                  Used for accessing user PII from Trellis API.
    onConnect: handleConnect,

    // OPTIONAL: onClose(error, metadata)
    // Called when the user closes the modal dialog.
    // - metadata
    //   - metadata.accountReferenceId - Account reference ID to use for searching Savvy.
    //                                   Currently set equal to Trellis Connection ID when
    //                                   Trellis Client ID is provided.
    //                                   May not be present if our servers could not be reached.
    onClose: handleClose,

    // OPTIONAL: onEvent(eventName, metadata)
    // Called when certain events happen. Supported event names:
    // - OPEN
    //     - The user has opened the widget.
    // - SELECT_ISSUER
    //     - The user has selected their insurance company.
    // - AUTH_COMPLETE
    //     - The user has finished login/authentication for an account.
    // - PROVIDE_CONSENT
    //     - The user has consented to Savvy's searching for offers.
    // - APPLICATION_COMPLETE
    //     - Enough data has been received that Savvy can get personalized offers.
    // - LOAD_OFFERS
    //     - The user has finished waiting for offers.
    // - CLICK_OFFER
    //     - The user clicked on a specific offer.
    // - TRANSITION_VIEW
    //     - When the Widget transitions between views.
    // - CLOSE
    //     - The flow has been exited. Also calls `onClose` callback.
    // - ERROR
    //     - If an error happens during the flow.
    onEvent: handleSavvyEvent,
  });
</script>
```
