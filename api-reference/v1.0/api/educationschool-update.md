---
title: "Update educationSchool"
description: "Update the properties of an educationSchool object."
author: "mlafleur"
localization_priority: Normal
ms.prod: "education"
doc_type: apiPageType
---

# Update a School

Namespace: microsoft.graph

Update the properties of an [educationSchool](../resources/educationschool.md) object.

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
PATCH /education/schools/{educationSchoolId}
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

In the request body, supply a JSON representation of the [educationSchool](../resources/educationschool.md) object.

The following table shows the properties that are required when you update the [educationSchool](../resources/educationschool.md).

| Property             | Type                                               | Description                                                                                                                                                                                        |
| :------------------- | :------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| displayName          | String                                             | Display name of the school. Inherited from [educationOrganization](../resources/educationorganization.md)                                                                                          |
| description          | String                                             | Description of the school. Inherited from [educationOrganization](../resources/educationorganization.md)                                                                                           |
| externalSource       | educationExternalSource                            | Source where this organization was created from. Inherited from [educationOrganization](../resources/educationorganization.md). Possible values are: `sis`, `manual`, `unknownFutureValue`, `lms`. |
| externalSourceDetail | String                                             | The name of the external source this resources was generated from.                                                                                                                                 |
| principalEmail       | String                                             | Email address of the principal.                                                                                                                                                                    |
| principalName        | String                                             | Name of the principal.                                                                                                                                                                             |
| externalPrincipalId  | String                                             | ID of principal in syncing system.                                                                                                                                                                 |
| highestGrade         | String                                             | Highest grade taught.                                                                                                                                                                              |
| lowestGrade          | String                                             | Lowest grade taught.                                                                                                                                                                               |
| schoolNumber         | String                                             | School Number.                                                                                                                                                                                     |
| externalId           | String                                             | ID of school in syncing system.                                                                                                                                                                    |
| phone                | String                                             | Phone number of school.                                                                                                                                                                            |
| fax                  | String                                             | Fax number of school.                                                                                                                                                                              |
| createdBy            | [identitySet](../resources/identityset.md)         | Entity who created the school.                                                                                                                                                                     |
| address              | [physicalAddress](../resources/physicaladdress.md) | Address of the school.                                                                                                                                                                             |

## Response

If successful, this method returns a `200 OK` response code and an updated [educationSchool](../resources/educationschool.md) object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_educationschool"
}
-->

```http
PATCH https://graph.microsoft.com/v1.0/education/schools/{educationSchoolId}
Content-Type: application/json
Content-length: 583

{
  "@odata.type": "#microsoft.graph.educationSchool",
  "displayName": "String",
  "description": "String",
  "externalSource": "String",
  "externalSourceDetail": "String",
  "principalEmail": "String",
  "principalName": "String",
  "externalPrincipalId": "String",
  "lowestGrade": "String",
  "highestGrade": "String",
  "schoolNumber": "String",
  "externalId": "String",
  "phone": "String",
  "fax": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "address": {
    "@odata.type": "microsoft.graph.physicalAddress"
  }
}
```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.educationSchool",
  "id": "1c23c12e-c12e-1c23-2ec1-231c2ec1231c",
  "displayName": "String",
  "description": "String",
  "externalSource": "String",
  "externalSourceDetail": "String",
  "principalEmail": "String",
  "principalName": "String",
  "externalPrincipalId": "String",
  "lowestGrade": "String",
  "highestGrade": "String",
  "schoolNumber": "String",
  "externalId": "String",
  "phone": "String",
  "fax": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "address": {
    "@odata.type": "microsoft.graph.physicalAddress"
  }
}
```
