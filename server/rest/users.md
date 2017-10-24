# Users

Methods for manage User model objects and associated models.

## GET User Data

Returns single profile, associated with certain user by token.

    GET /users/{user_id}

**`user-token` required. For more information about request headers see [API Welcome page](/server/api.md).**

**Response Example**

    {
        "id": 1,
        "name": "John",
        "lastname": "Appleseed",
        "company": "Apple",
        "position": "Employee",
        "email": "john@apple.com",
        "phone": "1234567890",
        "photo": "http://cocoaheads.ru/resources/photos/john_appleseed.jpg"
    }

## POST Create User Object

Creates new User instance in Database and returns it.

    POST /users

**Request Body Parameters**

|Name|Type|Value Description|Required|
|---|---|---|---|
|name|string|User first name|YES|
|lastname|string|User last name|YES|
|email|string|User email address|YES|
|phone|string|User phone|NO|
|company|string|User company name|NO|
|position|string|User position in company|NO|
|photo|string|User photo|NO|

**Response Example**

With only required parameters.

    {
        "id": 1,
        "name": "John",
        "lastname": "Appleseed",
        "company": "",
        "position": "",
        "email": "john@apple.com",
        "phone": "",
        "photo": ""
    }

## PATCH Update User Data

Updates User parameters, which were sent in body. Returns updated User.

    PATCH /user/{user_id}

**`user-token` required. For more information about request headers see [API Welcome page](/server/api.md).**

**Request Body Parameters**

|Name|Type|Value Description|Required|
|---|---|---|---|
|name|string|User first name|NO|
|lastname|string|User last name|NO|
|email|string|User email address|NO|
|phone|string|User phone|NO|
|company|string|User company name|NO|
|position|string|User position in company|NO|
|photo|string|User photo|NO|

**Response Example**

    {
        "id": 1,
        "name": "John",
        "lastname": "Appleseed",
        "company": "Apple",
        "position": "Employee",
        "email": "john@apple.com",
        "phone": "1234567890",
        "photo": "http://cocoaheads.ru/resources/photos/john_appleseed.jpg"
    }

## POST Register Push-Notifications for User

Register User token for receiving push-notifications. Creates new instance of `Clients` model in database.

    POST /users/clients

**`user-token` required. For more information about request headers see [API Welcome page](/server/api.md).**

**Request Parameters**

|Name|Value Type|Value Description|Required|
|---|---|---|---|
|push_token|String|Device token|YES|

**Response Example**