
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const directoryObject = {
  @odata.id:"https://graph.microsoft.com/beta/users/alexd@contoso.com"
};

let res = await client.api('/groups/{id}/rejectedSenders/$ref')
	.version('beta')
	.post({directoryObject : directoryObject});

```