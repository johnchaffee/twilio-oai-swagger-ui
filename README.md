# twilio-oai-swagger-ui

This repo renders the [Twilio Open API Spec](https://github.com/twilio/twilio-oai) in [Swagger UI](https://github.com/swagger-api/swagger-ui). Twilio publishes many APIs. This one renders the [twilio_api_v2010](https://github.com/twilio/twilio-oai/blob/main/spec/json/twilio_api_v2010.json) spec, which is used for managing phone numbers, sending messages, etc.

- [View the Twilio Open API Swagger UI](http://johnchaffee.wiki/twilio-oai-swagger-ui/)
- [View the Quick Start Video](http://johnchaffee.wiki/twilio-oai-swagger-ui/swagger.mp4)

## Requirements

- A Twilio Account
- A `TWILIO_ACCOUNT_SID` and `TWILIO_AUTH_TOKEN` 
- A Twilio Phone Number

## Instructions

- [View the Swagger doc](http://johnchaffee.wiki/twilio-oai-swagger-ui/)
- Click the Authorize button on the top right and enter your `TWILIO_ACCOUNT_SID` and `TWILIO_AUTH_TOKEN` as the username and password.
- Click the method you want to run to expand it.
  - For example, to send an SMS click on the [CreateMessage](./#/default/CreateMessage) method at the path `POST /2010-04-01/Accounts/{AccountSid}/Messages.json`
- Click the `Try it out` button
  - Fill in the required parametes (e.g. `AccountSid`, `Body`, `From`, `To`)
  - Uncheck all of the `Send empty value` checkboxes.
- Click `Execute` to invoke the API. With luck, your SMS message will be sent.

**NOTE**: You MUST uncheck ALL of the `Send empty value` checkboxes. Otherwise the API request will fail with a 400 Bad Request status and an obscure error message. To fix it, uncheck all of the `Send empty value` checkboxes and try again.

```json
{
  "code": 20001,
  "message": "invalid literal for int() with base 10: ''",
  "more_info": "https://www.twilio.com/docs/errors/20001",
  "status": 400
}
```