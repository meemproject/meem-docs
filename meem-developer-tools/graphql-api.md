# GraphQL API

The core Meem team maintains a service that indexes information about Meem contracts and tokens. These are the same GraphQL endpoints used by Clubs and [EPM](../epm/ethereum-package-manager.md).

{% hint style="info" %}
Any GraphQL query can be swapped out for a subscription! Just change `query` to `subscription`
{% endhint %}

#### GraphQL Explorer:&#x20;

[Polygon Mainnet](https://cloud.hasura.io/public/graphiql?endpoint=https%3A%2F%2Fgql.meem.wtf%2Fv1%2Fgraphql)

[Rinkeby](https://cloud.hasura.io/public/graphiql?endpoint=https%3A%2F%2Fdev-gql.meem.wtf%2Fv1%2Fgraphql)

#### GraphQL Endpoints:

Polygon Mainnet: [https://gql.meem.wtf/v1/graphql](https://gql.meem.wtf/v1/graphql)

Rinkeby: [https://dev-gql.meem.wtf/v1/graphql](https://dev-gql.meem.wtf/v1/graphql)

* _Note: Because Rinkeby is being deprecated, we will be migrating to Göerli in the near future_

_In the future, the plan is to decentralize this data_
