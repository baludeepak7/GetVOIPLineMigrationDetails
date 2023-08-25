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

  
