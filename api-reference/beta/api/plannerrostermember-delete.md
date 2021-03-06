---
title: "Delete plannerRosterMember"
description: "Deletes a plannerRosterMember object."
author: "tarkansevilmis"
localization_priority: Normal
ms.prod: "planner"
doc_type: apiPageType
---

# Delete plannerRosterMember
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Delete a [plannerRosterMember](../resources/plannerrostermember.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Tasks.ReadWrite|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /planner/rosters/{plannerRosterId}/members/{plannerRosterMemberId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "delete_plannerrostermember"
}
-->
``` http
DELETE https://graph.microsoft.com/beta/planner/rosters/523a9d5a-f9d5-45c1-929f-b8525393515c/members/5ba84f7a-aa11-4a51-a298-9f2c7ec6bb38
```


### Response
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

