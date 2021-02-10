---
title: "Add administrativeUnit"
description: "Add administrativeUnit by posting to the administrativeUnit collection."
author: "mmast"
localization_priority: Normal
ms.prod: "edicatopm"
doc_type: apiPageType
---

# Add administrativeUnit

Namespace: microsoft.graph

Add administrativeUnit by posting to the administrativeUnit collection.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | Not supported.                              |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | EduRoster.ReadWrite.All                     |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
POST /education/classes/{educationClassId}/members/{educationUserId}/schools/{educationSchoolId}/administrativeUnit/$ref
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

In the request body, supply a JSON representation of the [administrativeUnit](../resources/administrativeunit.md) object.

The following table shows the properties that are required when you create the [administrativeUnit](../resources/administrativeunit.md).

| Property    | Type   | Description                                                                                               |
| :---------- | :----- | :-------------------------------------------------------------------------------------------------------- |
| displayName | String | Display name of the school. Inherited from [educationOrganization](../resources/educationorganization.md) |
| description | String | Description of the school. Inherited from [educationOrganization](../resources/educationorganization.md)  |

## Response

If successful, this method returns a `204 No Content` response code and an [administrativeUnit](../resources/administrativeunit.md) object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_administrativeunit_from_"
}
-->

```http
POST https://graph.microsoft.com/v1.0/education/classes/{educationClassId}/members/{educationUserId}/schools/{educationSchoolId}/administrativeUnit/$ref
Content-Type: application/json
Content-length: 187

{
  "@odata.type": "#microsoft.graph.administrativeUnit",
  "deletedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "visibility": "String"
}
```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.administrativeUnit"
}
-->

```http
HTTP/1.1 204 No Content
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.administrativeUnit",
  "id": "03e281d6-81d6-03e2-d681-e203d681e203",
  "deletedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "visibility": "String"
}
```
