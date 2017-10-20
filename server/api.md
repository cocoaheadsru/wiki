# API

Here you can find all the necessary information about CocoaHeads Server REST API. We highly encourage you to read it carefully before contributing.

**If you contribute to CocoaHeads Server API and change API methods, you need to update this documentation as well.**

## Base URL

When you setup CocoaHeads Server on your local machine, you'll have 3 environments: Develop, Staging and Production.

Depending on environments base url will be:

- Develop: `http://localhost:8080/method/`
- Staging: ``
- Production: `http://upapi.ru/method/`

## Request Headers

Each request must include `token` string, which is current user token from CocoaHeads Meetup app. If user is not logged in `token` need to be empty string.

While debugging you can include `debug: 1` to headers. In debug mode response will contain additional information necessary for debugging.