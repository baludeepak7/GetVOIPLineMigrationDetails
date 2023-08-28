GetVOIPLineMigrationDetails

Service Description
===================

The service is part of the integration flow “Resource Provisioning”.This operation allows service consumers to enquire about the Customer’s Migration Status (‘Migration Phases’ and ‘Migration Activities’) and ‘Migration Data’ (‘Migration Line Features’ and ‘Migration Workorder Details’ from Midas. This service getting the mentioned details from MiDaS by calling a ‘Stored Procedure’.

An optional ‘context’ parameter can be used to limit the returned ‘Migration Status’ data for a specific functionality. In the absence of this optional parameter context ‘MIGRATION_PHASE’ would be used as a default context by this service.

Following describes the valid context options for this service and the corresponding ‘Migration Status’ details it will return when used in the service request:
    • Context ‘MIGRATION_PHASE’ is to be used to get the ‘Migration Phase’ details.
    • Context ‘MIGRATION_ACTIVITY’ is to be used to get the ‘Migration Activity’ details.
    • Context ‘MIGRATION_LINE_FEATURES’ is to be used to get the ‘Migration Line Features’ details.
    • Context ‘MIGRATION_WORKORDER’ is to be used to get the ‘Migration Workorder’ details.

Note: This service response time is only guaranteed when this service is called with a context, hence it is recommended for consumers of this service are to call this service with the relevant context.

### Request Header

  
service - Identifies the name of the service. For non-service messages (such as notifications), identifies a "logical destination or topic "
  
operation - Identifies the operation to be performed.

 version - Identifies the service version.
  
  conversationID - ConversationID is a unique identifier that remains unchanged for a complete business process and will be propagated  through all requests connected  with the business process.

  requestID - RequestID is a unique identifier that is unique for a single request or response message and will be used to map long and error message to consumer's request.
  
  messageID - messageID is a unique identifier that is unique for a request or response message but exists within a sequence for invoked/composed services. messageID can be consider a sequence identifier.
  
  requestTimestamp - Used to reflect the time when the message was created.

  activityName - Identifies the name of the business transaction activity for the message being exchanged.The value corresponds the business process or use case.

  senderURI - Identifies the system or application sending the message.

  originatorURI - Identifies the originator of the business process.

  replyToURI - Used by request messages to specify destination for response message.

  failureToURI - Identifies the application recieving the potential error notification message.

  userId - USER ID to identify applicant.

  security - Contains confidential information used to secure message proccessing.

  securityType - Identifies the type of credential in the security element.

  priority - Indicates message handling priority for messages.

### Query Parameters

telephoneNumber - Yes Telephone number, including any international dialling codes.
