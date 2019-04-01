## RapidPro Integration ##
 
 
RapidPro allows organizations to visually build scalable interactive messaging applications. RapidPro is a hosted service for visually building interactive messaging applications. To learn more, please visit the project site at http://rapidpro.github.io/rapidpro​.
Dozens of channels are supported in collaboration with SMS Companies and social networks that communicates across different ways inside RapidPro. The integration in RapidPro can be basically done in two ways, by using a REST API or an SMSC connection.

### 1. REST API ###

RapidPro easily connects with many channels by using an HTTP API, that will be available to all the workspaces to add channels of the same aggregator. SMS Aggregator needs to provide the following information to integrate:

- Full documentation about their public API, that includes authentication methods, input parameters and output format for each endpoint;
- A test phone number provided by aggregator;
- Access to a test account on the aggregator console to enable
developers to validate the integration when developing;
- The support team contacts from SMS Aggregator available to solve
any doubt about integration;

### 2. SMSC Connection ###

In the case of an SMSC connection, it's necessary to connect on a Virtual Private Network (VPN), because of security issues, so Ilhasoft guides the process to help clients to make these connections safely. There are many protocols that can be integrated, such as SMPP, UCP/EMI and CIMD2, it depends on what the SMS aggregator provides for 3rd party integration.

The first step to integrate depends on SMS aggregator, so it needs to provide the following items:

**Documentation**: The documentation necessary to connect to the aggregator VPN, send and receive messages through its services;

**Virtual Private Network (VPN) form**: Typically the SMS aggregator has a form that requires information from the company that wants to communicate with their services through a VPN connection, in this case Ilhasoft;

**SMSC Credentials**: Ilhasoft needs username, password, port and any
other information that's necessary to send and receive messages for the aggregator;

Once the above items are fully-filled, Ilhasoft connects to the VPN and notify the aggregator to route incoming messages to Ilhasoft server and the testing phase is initiated. During these phases is necessary to contact members of Ilhasoft team directly, so the following contacts can be used:

- Skype: john_dcc
- Email: john.dalton@ilhasoft.com.br
