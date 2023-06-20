# Getting Started

Since the Meem website is open source, you will be building your extension directly inside of our codebase and creating a pull request to have it merged into our app. **In the future, you will be able to create extensions without needing to use the meem app.**

{% hint style="info" %}
[https://github.com/meemproject/meem-app](https://github.com/meemproject/meem-app)
{% endhint %}

#### **Setting up your local environment**

1. Download this repository using the `git` client of your choice
2. In the root directory, run `yarn` to install dependencies
3. Copy `.env.example` and rename it to `.env`
4. Obtain an Alchemy API key and RPC URLs (or contact us to use ours!), then add them to the `.env` file
5. Run `yarn local` to run the app
6. Access the app at [http://localhost:3001](http://localhost:3001/)



#### **Add your extension to the Meem Extension database**

In order to enable your extension for testing, we'll need to add it to the Meem Extension database.

Just shoot us a message on on [Discord](https://discord.gg/RYwC9Rxy) and include the following information:\


> **Name:**\
> **Company:**\
> **What will your extension do?:**
>
> **What components will your extension use?:** See What&#x20;
>
> **Extension Name**: _The publicly visible name of your extension e.g. "My Extension"_\
> **Slug:** _This will be the slug used to access your extension pages e.g. "my-extension"_\
> **Description**: _This is the description users will see when exploring extensions e.g. "Do cool stuff with the My Extension Extension"_

_Note: You'll a PNG icon asset (visible in light and dark mode) at some point too._
