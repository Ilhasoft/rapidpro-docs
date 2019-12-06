You can connect an external aggregator or messaging service to the platform using our external API. To know how to add a channel you can read this article. When you finished the process to add an external channel, you will see this form.

![](/img/channel/channel7.png)

**URN Type**: You can choose what kind of unique identifier you want to use in the External Channel, there are several options available as Telegram or Facebook Identifiers, however, if you are using the external channel for SMS, you need to select Phone Number. You can also select External Identifier which means that you can use a custom identifier in these contacts;

**Number:** You can fill out this field with an identifier that's used as a source of the communication when sending messages when using External Channel for SMS companies you will put a short-code as a phone number;

**Country:** The country that the short-code belongs, that's used for validations in destination phone numbers;

**Method:** The method selected here is related to the HTTP method used to make requests of outgoing messages to this channel;

**Encoding:** This is the encoding method used for outgoing messages, it's available in 3 options:

**Default Encoding:** No conversion or formatting is applied to the text message;

**Smart Encoding:** A conversion is applied to outgoing messages which use the standard alphabet for SMS messages, written up in the standard GSM 03.38. It is always supported on GSM networks;

**Content-type:** The Content-Type that's used when sending the request, this is appended to the Header and the request body needs to follow the standard chosen;

**Max Length:** The maximum length of any single message on this channel (longer messages will be split). If you are connecting to an SMS aggregator, you need to ask them what's the maximum length used to send messages, otherwise, it can lead to errors when trying to send messages with higher size;

**Send URL:** The URL we will call when sending messages, with variable substitutions. Example: https://sms.aggregator.com/testing/test.php?text={{text}}

**Request Body:** The request body if any, with variable substitutions (only used for PUT or POST) for outgoing messages. Remember to put in the same format you configured as content-type in the previous field. There are many variables that can be used in the request body, but none of them are required by the platform, it depends on the aggregator which is delivering the message, these are the variables available:

**id:** Unique id for messages created by the platform. Example: 4456783

**text:** The text message that will be sent to contacts with its respective encoding handled;

**to:** Destination phone number in international format. Example: +5582999566247;

**to_no_plus:** Destination phone number without the plus sign. Example: 5582999566247

**from:** Source phone number or short-code in international format. Example: +64128;

**from_no_plus:** Source phone number or short-code without plus sign. Example: 64128;

**channel:** Channel Identifier responsible for each message. Example: 33758bf9-4bb0-4378-9859-0e5845ea6dfd;

**MT Response Check:** This is a field that you can use to validate aggregator's responses, if the content filled in this field is not available in the response, the platform will consider that as an error;