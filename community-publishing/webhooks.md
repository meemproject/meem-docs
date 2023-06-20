# Webhooks

When creating a new publishing flow on Meem, you may choose to publish approved posts to a webhook. Webhooks enable you to manage the output of approved messages as you see fit.

### Setting up a Webhook Publishing Flow

To establish a flow that publishes to a webhook, first ensure that you've onboarded your community with Meem:[https://app.meem.wtf/onboard/symphony](https://app.meem.wtf/onboard/symphony)

Once you've added the Meem bot to your community Discord or Slack, you can create a new flow from your community dashboard by clicking the "**+ Add New Flow**" button.

When setting up your new publishing flow, select "**Add a custom webhook**" from the publishing options

<figure><img src="../.gitbook/assets/Screen Shot 2023-04-02 at 10.30.12 PM.png" alt=""><figcaption></figcaption></figure>

After selecting the webhook publishing option, you will see an input field where you can enter your webhook's URL. Make sure to include the full URL, including https://

<figure><img src="../.gitbook/assets/Screen Shot 2023-04-02 at 10.31.38 PM.png" alt=""><figcaption></figcaption></figure>

You will also receive a private key that is generated for your webhook. Be sure to save this key since you will not be able to view it again from the dashboard. Your private key will be sent along with the data object to your webhook endpoint whenever your publishing flow is triggered so that you can verify that the request is coming from the Meem API.

Below is an example of the data that gets sent to a webhook via a `POST` request when a publishing flow is approved.

```json
"body": {
    "reactions": [
        {
            "name": "👍",
            "emoji": "👍",
            "unicode": "1f44d",
            "count": 1
        }
    ],
    "createdTimestamp": 1680294663760,
    "user": {
        "id": "555555555555555555", // the user id of the input platform (see rule input)
        "username": "coolbeans123"
    },
    "secret": "c06b8a4d-4cce-4fb6-acd9-10a7cb94534d", // private key
    "attachments": [
        {
            "url": "https://hereisaninterestinglink.com",
            "name": "An interesting link...",
            "description": "This is very interesting indeed..."
        }
    ], // media and links that were associated with the approved content
    "channelId": "55555555555555555",
    "totalApprovals": 1,
    "totalProposers": 0,
    "totalVetoers": 0,
    "rule": {
        "votes": 1,
        "isEnabled": true,
        "publishType": "publishImmediately",
        "vetoerRoles": [],
        "vetoerEmojis": [],
        "approverRoles": [
            "55555555555555555"
        ],
        "approverEmojis": [
            "1f44d"
        ],
        "proposerEmojis": [],
        "proposalChannels": [
            "555555555555555555"
        ],
        "input": "discord", // The input source e.g. slack | discord
        "output": "webhook",
        "inputRef": "de57d570-c46d-4859-82f5-5cf9b22ee44d",
        "outputRef": null
    },
    "content": "Here is a very interesting comment. https://hereisaninterestinglink.com"
}
```
