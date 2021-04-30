# Conversations Quickstart App for Android

This is a lightweight Android application for [Twilio Conversations](https://www.twilio.com/docs/conversations).

# Configuring and getting started

This demo requires a Twilio account and a working Conversations Service SID.
Here is what is needed:

* Your Account's Conversation Service Sid `ISXXX` SID which is attached to your Conversation Service. You can find that information in the [Twilio Console](https://www.twilio.com/console/conversations/services). You can also create a service there if you don't already have one.

# Replacing the Access Token
In order for your quickstart application to work, we need to authenticate an end user by retrieving a short-lived access token attached to your API Key. The `strings.xml` resource has a placeholder for your access token named  `test_access_token`.

You can generate a token in a few ways:
* Using the [twilio-cli](https://www.twilio.com/docs/twilio-cli/quickstart) and [twilio token plugin](https://github.com/twilio-labs/plugin-token) (Recommended)
* Using [Twilio Runtime Function](https://www.twilio.com/docs/runtime/functions)

 For the twilio-cli option, run the following command and enter the resulting token into the placeholder:
 
 `twilio token:chat --identity <The test username> --chat-service-sid <ISXXX...>`

Note: You need to generate an access token with a ChatGrant for a Conversations user to use the Twilio Conversations Client SDK.

After generating a token manually, it will expire after a timeout period, so you will need to replace the token. To use this in production software, you would typically create a token endpoint in your back end application that uses your existing user authentication strategy.
