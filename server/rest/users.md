# Users

## GET User Profile

Returns single profile, associated with certain user by token.


    GET /user/profile

**Request Parameters**

|Name|Value Type|Value Description|Required|
|---|---|---|---|
|token|String|User Device Token|YES|

**Response Data Structure**

|Property|Type|Description|Remarks|
|---|---|---|---|
|id|integer|||
|username|string|||
|email|string|||
|phone|string|||
|status|integer|10 — Active User<br>0 — Deleted User||

**Response Example**

    [
        {
            "id": 1,
            "user_id": 2,
            "position": 1,
            "photo_url": "zimin.jpg",
            "info": "Superstar",
            "url": "https://github.com/azimin",
            "active": 1
        }
    ]

## POST Edit User

Allows to edit User info.

    POST /user/edit

**Request Parameters**

|Name|Value Type|Value Description|Required|
|---|---|---|---|
|name|String|User first name|YES|
|last_name|String|User last name|YES|
|email|String|User email address|YES|
|phone|String|User phone|NO|
|company|String|User company name|NO|
|position|String|User position in company|NO|

**Response Data Structure**

**Response Example**

## POST Register Push-Notifications for User

Registering user token for receiving push-notifications.

    POST /user/register_push

**Request Parameters**

|Name|Value Type|Value Description|Required|
|---|---|---|---|
|push_token|String|Device token|YES|

**Response Data Structure**

**Response Example**