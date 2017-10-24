# API

Here you can find all the necessary information about CocoaHeads Server REST API. We highly encourage you to read it carefully before contributing.

**If you contribute to CocoaHeads Server API and change API methods, you need to update this documentation as well.**

## Base URL

When you setup CocoaHeads Server on your local machine, you'll have 3 environments: Develop, Staging and Production.

Depending on environments base url will be:

- Develop: `http://localhost:8080/`
- Staging: `http://dev.cocoaheads.ru`
- Production: `http://api.cocoaheads.ru/`

## Request Headers

Request must include following header parameters:

|Parameter|Type|Description|Required|
|---|---|---|---|
|api-version|string|Current version of API|YES|
|secret-token|string|App secret token (`test` for Develop environment)|YES|
|user-token|string|Current user token|YES*|

\* `user-token` required for several methods which return user specific data.