# Refresh ENS

The Meem API indexes ENS names for Wallets. You can also force a refresh. Note that this will just _queue the update_. It may still take some time before the name is refreshed and updated in our database.

{% swagger src="https://dev-api.meem.wtf/api/1.0/meem-api.json" path="/me/refreshENS" method="get" %}
[https://dev-api.meem.wtf/api/1.0/meem-api.json](https://dev-api.meem.wtf/api/1.0/meem-api.json)
{% endswagger %}
