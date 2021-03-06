---
title: "chat resource type"
description: "A chat is a collection of chatMessages between 1 or more participants"
author: "nkramer"
localization_priority: Normal
ms.prod: "microsoft-teams"
---

# chat resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A chat is a collection of [chatMessages](chatmessage.md) between 1 or more participants. Participants can be users or apps. 


## Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[List chats](../api/chat-list.md) | [chat](channel.md) collection | Get the list of chats a user is part of.|
|[Get chat](../api/chat-get.md) | [chat](channel.md) | Read properties and relationships of the chat.|
|[List messages in a chat](../api/chat-list-messages.md)  | [chatMessage](../resources/chatmessage.md) | Get messages in a 1:1 or group chat |
|[Get message in chat](../api/chat-get-message.md)  | [chatMessage](../resources/chatmessage.md) | Get a single message in a chat |


## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|String|The chat's unique identifier. Read-only.|
|topic|String| (Optional) Subject or topic for the chat. Only available for group chats|
|createdDateTime|dateTimeOffset| Date and time at which the chat was created. Read-only.|
|lastUpdatedDateTime|dateTimeOffset| Date and time at which the chat was updated. Read-only.|
|chatType|String| The tupe of chat. Supported values: MicrosoftTeams, Interop, Federation|

## Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|messages|[chatMessage](chatmessage.md) collection|A collection of all the messages in the chat. A navigation property. Nullable. Currently this API only supports reading but will eventually support writing messages too.|

## JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.chat"
}-->

```json
{
  "id": "string (identifier)",
  "topic": "string",
  "createdDateTime": "dateTimeOffset",
  "lastUpdatedDateTime": "dateTimeOffset",
  "chatType": "string"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "chat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}
-->
