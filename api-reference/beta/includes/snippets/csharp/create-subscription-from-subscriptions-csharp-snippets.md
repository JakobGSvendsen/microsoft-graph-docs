---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var subscription = new Subscription
{
	ChangeType = "updated",
	NotificationUrl = "https://webhook.azurewebsites.net/api/send/myNotifyClient",
	Resource = "me/mailFolders('Inbox')/messages",
	ExpirationDateTime = DateTimeOffset.Parse("2016-11-20T18:23:45.9356913Z"),
	ClientState = "secretClientValue"
};

await graphClient.Subscriptions
	.Request()
	.AddAsync(subscription);

```