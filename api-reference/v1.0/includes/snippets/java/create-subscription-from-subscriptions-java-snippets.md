---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Subscription subscription = new Subscription();
subscription.changeType = "updated";
subscription.notificationUrl = "https://webhook.azurewebsites.net/api/send/myNotifyClient";
subscription.resource = "me/mailFolders('Inbox')/messages";
subscription.expirationDateTime = "2016-11-20T18:23:45.9356913Z";
subscription.clientState = "secretClientValue";

graphClient.subscriptions()
	.buildRequest()
	.post(subscription);

```