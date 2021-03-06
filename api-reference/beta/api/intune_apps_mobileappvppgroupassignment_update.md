﻿# Update mobileAppVppGroupAssignment
Update the properties of a [mobileAppVppGroupAssignment](../resources/intune_apps_mobileappvppgroupassignment.md) object.
### Prerequisites
One of the following **scopes** is required to execute this API:

*DeviceManagementApps.ReadWrite.All*
### HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
```http
PATCH /mobileAppGroupAssignments/{id}
PATCH /deviceAppManagement/mobileApps/{id}/groupAssignments/{id}
```

### Request headers
|Header|Value|
|---|---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

### Request body
In the request body, supply a JSON representation of a [mobileAppVppGroupAssignment](../resources/intune_apps_mobileappvppgroupassignment.md) object.
The following table shows the properties that are required when you create a [mobileAppVppGroupAssignment](../resources/intune_apps_mobileappvppgroupassignment.md).

|Property|Type|Description|
|---|---|---|
|targetGroupId|String|The Id of the AAD group we are targeting the mobile app to. Inherited from [mobileAppGroupAssignment](../resources/intune_apps_mobileappgroupassignment.md)|
|id|String|Key of the entity. Inherited from [mobileAppGroupAssignment](../resources/intune_apps_mobileappgroupassignment.md)|
|installIntent|String|The install intent defined by the admin. Inherited from [mobileAppGroupAssignment](../resources/intune_apps_mobileappgroupassignment.md) Possible values are: `available`, `notApplicable`, `required`, `uninstall`, `availableWithoutEnrollment`.|
|useDeviceLicensing|Boolean|Whether or not to use device licensing.|



### Response
If successful, this method returns a `200 OK` response code and an updated [mobileAppVppGroupAssignment](../resources/intune_apps_mobileappvppgroupassignment.md) object in the response body.

### Example
##### Request
Here is an example of the request.
```http
PATCH https://graph.microsoft.com/beta/mobileAppGroupAssignments/{id}
Content-type: application/json
Content-length: 116

{
  "targetGroupId": "Target Group Id value",
  "installIntent": "notApplicable",
  "useDeviceLicensing": true
}
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 231

{
  "@odata.type": "#microsoft.graph.mobileAppVppGroupAssignment",
  "targetGroupId": "Target Group Id value",
  "id": "89a8674a-674a-89a8-4a67-a8894a67a889",
  "installIntent": "notApplicable",
  "useDeviceLicensing": true
}
```



