---
description: >-
  Welcome to Meem!  This section provides an overview of our protocol and
  developer tools.
---

# 👋 Introduction to Meem

### Who we are

We’re [**meem**](http://meem.wtf). Our protocol frees media from centralized platforms and connects people directly. By enabling communities to design and manage their own agreements, we’ll make the future internet more creative, inclusive, and equitable.&#x20;

We believe the future of media is person-to-person.

### What we’re building

We’re building the open-source [**Meem app**](https://app.meem.wtf) to act as the online home for any collection of people for any purpose. Our **meem protocol** allows people to create and manage **agreements** - or organizational structures. Interfacing between the Meem app and protocol is our **Meem API** and **SDK.**

An agreement acts as a community’s Web3 home base. Community leaders can set membership criteria, manage nuanced roles and permissions, and seamlessly issue tokens to authorized participants, no coding required. They can sync their favorite tools and apps to create a living dashboard for their members. Meem empowers these organizers to manage their community and its activities without dependence on centralized platforms.

In effect, Meem acts as a community operating system in the form of a meem protocol smart contract. Each community's agreement is actually a **contract address**, deployed and owned by its creator. The contract address operates as a group username granting members access across dApps, letting community members engage with DAO tools, token-gated content, governance, and more.

While Meem provides a no-code entry point for a community leader to create a contract address for their group, we’ve also built the [**Ethereum Package Manager (EPM)**](http://epm.meem.wtf) to allow for more contract customization under the hood. Using EPM, developers can modify the underlying contract for their club, setting even more nuanced roles, permissions, and rules.&#x20;

Community admins can use their contract address to connect to Web3 dApps, manually or (more seamlessly) through our integrations. Our first integrations center around access management (Guild), DAO/treasury management (Gnosis), collaborative docs (Sliksafe), and publishing tools (paragraph.xyz, Tabula, Farcaster, etc.). As we integrate, we're enabling a more detailed and powerful way of managing roles across the ecosystem.

### Meem Ecosystem

Each of our areas of focus are intertwined and build upon one another.

The [**Meem Protocol**](meem-contracts/meem-protocol.md) is the definition of primitives that can empower decentralized person-to-person and person-to-asset connections

The [**Meem Contracts**](broken-reference) are the implementation of the [**Meem Protocol**](meem-contracts/meem-protocol.md). These contracts are still generalized and can be applied in various specific ways. They can represent anything and may relate to one another.

The [**Meem App**](https://app.meem.wtf) is one specific implementation of how the [**Meem Contracts**](broken-reference) can define roles within an organization.

[**EPM**](epm/ethereum-package-manager.md) is a tool used to deploy and manage contracts. Behind the scenes, the Core Team uses it to manage upgrades for Clubs. It can also be used to deploy any contract through a web UI or manage any EIP-2535 diamond proxy contract.

{% hint style="info" %}
The **Meem Protocol** is the **idea**.

The **Meem Contracts** are the **implementation**.

All **Agreements** use **Meem Contracts**.

Not all **Meem Contracts** are **Agreements**.

**EPM** is a tool to manage Diamond Contracts

**EPM** can also be used to deploy any smart contract
{% endhint %}

##



