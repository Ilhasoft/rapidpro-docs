## SMS Integration

The platform allows organizations to visually build scalable interactive messaging applications. The platform is a hosted service for visually building interactive messaging applications. To learn more, please [visit the project site](http://rapidpro.github.io/rapidpro). Dozens of channels are supported in collaboration with SMS Companies and social networks that communicates across different ways inside the platform. The SMS integration can be basically done in two ways, by using a REST API or an SMSC connection.

### 1. Built-in Integration

This is the quickest way to integrate the SMS channel to the platform, as it has the built-in functionality of sending and receiving messages to External services already available to all workspaces. There are two parts of this integration:

**Outgoing Messages**

When we need to send an outgoing message it will make a POST to this URL with the parameters 'text', 'to', 'from', 'channel' and 'id'. Example:

POST https://google.com.br
Content-Type: application/json
Body:
{
    "id": 1241244,
    "text": "Love is patient. Love is kind.",
    "to": "+250788123123",
    "to_no_plus": "250788123123",
    "from": "+5582999489287",
    "from_no_plus": "5582999489287",
    "channel": 346
}

**Incoming Messages**

When a new message is received by your service, it should notify us with a POST to the following URL, passing the following parameters: 'from' and 'text'. Callers can optionally also send a 'date' parameter in ISO-8601 (ex: 2012-04-23T18:25:43.511Z) format to specify the time the message was received. Example:

POST https://rapidpro.ilhasoft.mobi/c/ex/a86f686f-9168-4dd9-a03e-77f11b265b56/receive
from=%2B250788123123&text=Love+is+patient.+Love+is+kind.&date=2012-04-23T18:25:43.511Z

### 2.REST API

The platform easily connects with many channels by using an HTTP API, that will be available to all the workspaces to add channels of the same aggregator. SMS Aggregator needs to provide the following information to integrate:

- Full documentation about their public API, that includes authentication methods, input parameters and output format for each endpoint;
- A test phone number provided by aggregator;
- Access to a test account on the aggregator console to enable developers to validate the integration when developing;
- The support team contacts from SMS Aggregator available to solve any doubt about integration;


### SMSC Connection

In the case of an SMSC connection, it's necessary to connect on a Virtual Private Network (VPN), because of security issues, so Ilhasoft guides the process to help clients to make these connections safely.  There are many protocols that can be integrated, such as SMPP, UCP/EMI and CIMD2, it depends on what the SMS aggregator provides for 3rd party integration.
The first step to integrate depends on SMS aggregator, so it needs to provide the following items:

**- Documentation:** The documentation necessary to connect to the aggregator VPN, send and receive messages through its services;

**- Virtual Private Network (VPN) form:** Typically the SMS aggregator has a form that requires information from the company that wants to communicate with their services through a VPN connection, in this case Ilhasoft;

**- SMSC Credentials:**  Ilhasoft needs username, password, port and any other information that's necessary to send and receive messages for the aggregator;

Once the above items are fully-filled, Ilhasoft connects to the VPN and notify the aggregator to route incoming messages to Ilhasoft server and the testing phase is initiated. During these phases is necessary to contact members of Ilhasoft team directly, so the following contacts can be used:

- Skype: john_dcc
- Email: john.dalton@ilhasoft.com.br