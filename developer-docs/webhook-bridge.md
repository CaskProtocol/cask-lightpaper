# Web Bridge

The Cask Web Bridge is an application the service provider/merchant can run that will translate on-chain events
about subscriptions to the provider's services into traditional webhooks as well as provide a REST API to query
information about the subscriptions.

Webhooks are triggered when on-chain events happen (such as new subscriptions, cancellations, renewals, etc...)
against the providers address and are delivered  via an HTTP `POST` request with a `json` body describing the event.

The REST API (coming soon) is provided to be able to query information about subscriptions such as the current status, billing, 
plan and other information.


## Setup

The web bridge is available at `<REPO LINK>` and as a docker image, which can be ran using the docker command:

```shell
docker run --name mybridge -e WEBSOCKET_PROVIDER=... -e WALLET_ADDRESS=0x... -e WEBHOOK_ENDPOINT=https://.... -d cask-web-bridge 
```


## Environment Variables

The following environment variables are used to configure the web bridge. If running the web bridge directly 
(instead of via docker), you can create a file called `.env` in the root of the project folder containing the 
environment variables.

| Name               |                                                          Description                                                          |
|--------------------|:-----------------------------------------------------------------------------------------------------------------------------:|
| WEBSOCKET_PROVIDER | Websocket URL to a web3 provider, such as infura or alchemy. Use a websocket (ws:// or wss://) URL, and not a json/https URL. |
| WALLET_ADDRESS     |                        Wallet address of the service provider/merchant, that is associated with Cask.                         |
| WEBHOOK_ENDPOINT   |                                               URL in which to deliver webhooks.                                               |
| CASK_ENVIRONMENT   |                     Valid values are `testnet` and `production`, if not specified, assumes `production`.                      |
| REST_API_PORT      |                         Port to use for REST API. Leave blank (or set to 0) to disable the REST API.                          |
| VERBOSE            |                              Set to `1` to enable verbose logging for troubleshooting purposes.                               |



## Webhook Event List


| Event                                       |                                  Description                                   |
|---------------------------------------------|:------------------------------------------------------------------------------:|
| [SubscriptionCreated](#subscriptioncreated) |                        A new subscription has been created                     |
| SubscriptionChangedPlan                     |                   An existing subscription has changed plans                   |
| SubscriptionPendingChangePlan               |      An existing subscription has scheduled a plan change at next renewal      |
| SubscriptionChangedDiscount                 |                  An existing subscription applied a discount                   |
| SubscriptionPaused                          |                           A subscription was paused                            |
| SubscriptionResumed                         |                           A subscription was resumed                           |
| SubscriptionPendingCancel                   |         A subscription was scheduled for cancellation at next renewal          |
| SubscriptionCanceled                        |                          A subscription was canceled                           |
| SubscriptionRenewed                         |               A subscription renewal was successfully processed                |
| SubscriptionTrialEnded                      |   A subscription that was in a trial ended the trial and converted to active   |
| SubscriptionPastDue                         | A subscription renewal was attempted but insufficient funds were able to renew |


## Argument Formatting

### Addresses

Addresses such as `consumer` and `provider` are the 42-character hexadecimal formatted address.

### Subscription ID

The `subscriptionId` field is a unique 32 byte hexadecimal value representing the subscription instance. It is also
the NFT tokenId of the subscription, and in some online tools will be formatted as a uint256 value instead of a hexadecimal
value.

This ID can be used to fetch the active subscription state from the blockchain directly.

### ref

The `ref` field is a 32 byte hexadecimal value that can be provided by the service provider/merchant at subscription
creation time via the [Javascript Widget](javascript-widget.md) `ref` parameter. The value must be supplied in hexadecimal format and always
be a full 32-byte value. There are several utilities provided in the `@caskprotocol/sdk` package to encode/decode strings, 
numbers and UUIDs into this value. If no value was provided via the widget, the ref value will be the zero value
`0x0000000000000000000000000000000000000000000000000000000000000000`.

### Plan ID

The `planId` field is the numeric identifier for the plan that is the currently active plan of the subscription.

### Discount ID

The `discountId` field contains the hash ID of the discount code that is applied to the subscription. This
value can be used to look up the discount from the provider profile IPFS data which uses the same hash ID. If
the subscription has no discount, the value is `0x0000000000000000000000000000000000000000000000000000000000000000`.

### Block

The `block` object contains details about the block in which the on-chain event was processed.


### Transaction Hash

The `transactionHash` field is the on-chain transaction ID which generated the event and can be used to look up the
event on blockchain explorers.

### Chain ID

The `chainId` field contains the blockchain ID for which blockchain originated the event.


## SubscriptionCreated

The `SubscriptionCreated` event is triggered when a consumer creates a subscription. 

### Arguments


| Name           |                   Description                    |
|----------------|:------------------------------------------------:|
| consumer       |               Address of consumer                |
| provider       |               Address of provider                |
| subscriptionId |              ID of new subscription              |
| ref            | Optional custom identifier for this subscription |
| planId         |           Plan ID of new subscription            |
| discountId     |              ID of applied discount              |


### Example Webhook Body

```json
{
  "event": "SubscriptionCreated",
  "args": {
    "consumer": "0xab60a9037EdA0F517125dd9f87CC5621D77a10b8",
    "provider": "0xf3d6495662b71212c9De76a15e6666E199a64B97",
    "subscriptionId": "0xb6f30c97fc59a64dea2384bbaf54cd61306e462266e76dc280feabe5016b7fd3",
    "ref": "0xa1c2b8080ed4b6f56211e0295659ef87dd454b0a884198c10384f230525d4ee8",
    "planId": 100,
    "discountId": "0x0000000000000000000000000000000000000000000000000000000000000000"
  },
  "block": {
    "number": 169,
    "hash": "0x824b7d46b4ce79fa8b8dd8ba0520c2c5364439a3f696da7007c0c696fc6d5c11",
    "parentHash": "0x40152c2bcf0e2fb9c83defc2c99e2fcd131886f4a3bb102d77a5acdc01d0e1bd",
    "timestamp": 1646685639,
    "difficulty": 131328
  },
  "transactionHash": "0xf32f03ee2212188ac010a2efe0d3f2226b0a354dfe74f5ccf1584da9ecbffe9d",
  "chainId": 137
}
```

