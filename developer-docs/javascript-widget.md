# Javascript Widget

## Overview

The Cask Checkout Button is a simple way to add a subscription to your website/web application and start accepting
non-custodial cryptocurrency payments. The button opens a widget that facilities all of the web3 interaction and currently
supports [Metamask](https://metamask.io/) and [WalletConnect](https://walletconnect.com/).

## Installation

Add the following to website or web application in a single place such as the head or near the end of the body tag.

```html
<script src="https://js.cask.fi/v1/index.js"></script>
```

## Usage

Each location on the page where it is desired to have a checkout button, place the following tag:

```html
<cask-checkout-button
  class="cask-checkout-button"
  provider="0x...."
  plan="123456"
  environment="integration"
  onClose="close"
  onSuccess="success"
  label="Checkout with Crypto"
></cask-checkout-button>
```

### Attributes:

| name        | Required |                                                                                Description |
|-------------|:--------:|-------------------------------------------------------------------------------------------:|
| provider    |    ✔     |                                                    Wallet address of the service provider. |
| plan        |    ✔     |                                                   The Cask plan ID in which to subscribe . |
| environment |          |     Environment. Possible values: `integration` or `production`. Defaults to `production`. |
| class       |          |                                                                      CSS class(es) to add. |
| label       |          |                                                                Label to put on the button. |
| ref         |          |                         Include a custom value associated with the Cask subscription data. |
| size        |          |         Button size. Possible values:`regular`, `large` or `small`. Defaults to `regular`. |
| theme       |          |                      Widget theme. Possible values: `dark` or `light`. Defaults to `dark`. |
| redirect    |          | Redirect to URL upon successful subscribe. Does not call `onSuccess` handler, if supplied. |
| onClose     |          |                                                            Callback when widget is closed. |
| onSuccess   |          |                                                    Callback after successful subscription. |



### Styling:

It is possible to override all styles of `cask-checkout-button` by using the [Shadow CSS ::part](https://github.com/fergald/docs/blob/master/explainers/css-shadow-parts-1.md) spec. 
Target the `button` "::part" in the styles, such in the example below:

```html

<style>
    .cask-checkout-button::part(button) {
        background-color: #2c95e0;
        font-size: 24px;
    }
    .cask-checkout-button::part(button):hover {
        box-shadow: inset 0 0 20px 20px rgb(0 0 0 / 15%);
    }
</style>
<cask-checkout-button
        class="cask-checkout-button"
        provider="0x...."
        plan="123456"
        label="Pay with Crypto"
></cask-checkout-button>
```

See more `::part()` documentation at https://developer.mozilla.org/en-US/docs/Web/CSS/::part


### Callbacks:

The following callbacks are supported:
* `onClose` - _No parameters_ :: Called when the widget is closed.
* `onSuccess` - _(txn)_ :: Called after a successful subscription
  * `txn` - On-chain transaction ID of the subscription transaction
  
```html
<cask-checkout-button
  class="cask-checkout-button"
  provider="0x...."
  plan="123456"
  environment="integration"
  onClose="caskClose"
  onSuccess="caskSuccess"
  label="Checkout with Crypto"
></cask-checkout-button>
```

```html
<script type="application/javascript">
    function caskClose() {
        console.log("Cask widget closed");
    }
    
    function caskSuccess(txn) {
        console.log("Cask subscription successful. Transaction: " + txn);
    }
</script>
```