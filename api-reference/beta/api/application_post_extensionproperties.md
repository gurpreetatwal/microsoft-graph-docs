# Create extensionProperty

Use this API to create a new extensionProperty.
## Prerequisites
One of the following **scopes** is required to execute this API: *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*
## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /applications/{id}/extensionProperties

```
## Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer &lt;token&gt; *Required*  |

## Request body
In the request body, supply a JSON representation of [extensionProperty](../resources/extensionproperty.md) object.


## Response
If successful, this method returns `201, Created` response code and [extensionProperty](../resources/extensionproperty.md) object in the response body.

## Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_extensionproperty_from_application"
}-->
```http
POST https://graph.microsoft.com/beta/applications/{id}/extensionProperties
Content-type: application/json
Content-length: 231

{
  "extensionProperty": {
    "appDisplayName": "appDisplayName-value",
    "name": "name-value",
    "dataType": "dataType-value",
    "isSyncedFromOnPremises": true,
    "targetObjects": [
      "targetObjects-value"
    ]
  }
}
```
In the request body, supply a JSON representation of [extensionProperty](../resources/extensionproperty.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.extensionproperty"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 253

{
  "extensionProperty": {
    "appDisplayName": "appDisplayName-value",
    "name": "name-value",
    "dataType": "dataType-value",
    "isSyncedFromOnPremises": true,
    "targetObjects": [
      "targetObjects-value"
    ],
    "id": "id-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create extensionProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->