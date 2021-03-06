# Ballerina Salesforce REST Connector

The salesforcerest connector allows you to access the Salesforce REST API through ballerina. And the salesforcerest 
connector actions are being invoked by a ballerina main function. The following section provide you the details on how 
to use Ballerina Salesforce REST connector.

## Getting started

1. Download the Ballerina tool distribution by navigating https://ballerinalang.org/downloads/
2. Navigate to https://github.com/ballerinalang/connector-oauth2/releases
   Download and Extract ballerina-oauth2-0.95.0.zip and copy ballerina-oauth2-0.95.0.jar into the `<ballerina-tools>/bre/lib` folder.
3. Extract ballerina-salesforcerest-0.95.0.zip and copy ballerina-salesforcerest-0.95.0.jar into the `<ballerina-tools>/bre/lib` folder.

##### Prerequisites
1. Create a Salesforce organization and create a connected app by visiting [Salesforce](https://login.salesforce.com/)
2. Obtain the following parameters
    * Client Id
    * Client Secret
    * Access Token
    * Refresh Token
    * Api Instance
    * Api Version
    * Refresh endpoint

Refresh endpoint :-
Sandbox Organization - https://test.salesforce.com/services/oauth2/token
Other Organization - https://login.salesforce.com/services/oauth2/token

**IMPORTANT** This access token and refresh token can be used to make API requests on your own
account's behalf. Do not share your access token, client  secret with anyone.


## Working with Salesforce REST connector actions

##### describeGlobal
Lists the available objects and their metadata for your organization’s data

###### Properties

###### Related Salesforce documentation
[describeGlobal](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_describeGlobal.htm)

##### sObjectDescribe
"Completely describes the individual metadata at all levels for the specified object"

###### Properties
* sobjectName - The relevant sobject name

###### Related Salesforce documentation
[sObjectDescribe](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_describe.htm)

##### listAvailableApiVersion
Lists summary information about each REST API version currently available

###### Properties

###### Related Salesforce documentation
[listAvailableApiVersion](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_versions.htm)

##### listOrganizationLimits
Lists limits information for your organization

###### Related Salesforce documentation
[listOrganizationLimits](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_limits.htm)

##### listResourcesByApiVersion
Lists the resources available for the specified API version

###### Properties
* apiVersion - The api version to get resources

###### Related Salesforce documentation
[listResourcesByApiVersion](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_discoveryresource.htm)

##### sObjectBasicInfo
Describes the individual metadata for the specified object

###### Properties
* sobjectName - The relevant sobject name

###### Related Salesforce documentation
[sObjectBasicInfo](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_basic_info.htm)

##### sObjectGetDeleted
Retrieves the list of individual records that have been deleted within the given timespan for the specified object

###### Properties
* sobjectName - The relevant sobject name
* startTime - The start time of the time span
* endTime - The end time of the time span

###### Related Salesforce documentation
[sObjectGetDeleted](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_getdeleted.htm)

##### sObjectGetUpdated
Retrieves the list of individual records that have been updated (added or changed) within the given timespan for the specified object

###### Properties
* sobjectName - The relevant sobject name
* startTime - The start time of the time span
* endTime - The end time of the time span

###### Related Salesforce documentation
[sObjectGetUpdated](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_getupdated.htm)

##### sObjectPlatformAction
Query for actions displayed in the UI, given a user, a context, device format, and a record ID

###### Related Salesforce documentation
[sObjectPlatformAction](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_platformaction.htm)

##### sObjectRows
Accesses records based on the specified object ID

###### Properties
* sobjectName - The relevant sobject name

###### Related Salesforce documentation
[sObjectRows](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_retrieve.htm)

##### sObjectRowsByExternalId
Creates new records or updates existing records (upserts records) based on the value of a specified external ID field

###### Properties
* sobjectName - The relevant sobject name
* fieldId - The external field id"
* fieldValue - The external field value

###### Related Salesforce documentation
[sObjectRowsByExternalId](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_upsert.htm)

##### listviewQueryPerformanceFeedback
Get feedback on how Salesforce will execute your list view

###### Properties
* listViewId - The id of the listview to get the feedback from

###### Related Salesforce documentation
[listviewQueryPerformanceFeedback](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_query_explain.htm)

##### query
Executes the specified SOQL query

###### Properties
* queryString - The request SOQL query

###### Related Salesforce documentation
[query](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_query.htm)

##### queryAll
QueryAll will return records that have been deleted because of a merge or delete, archived Task and Event records

###### Properties
* queryString - The request SOQL query

###### Related Salesforce documentation
[queryAll](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_queryall.htm)

##### queryAllMore
If the queryAll results are too large, retrieve the next batch of results

###### Properties
* nextRecordsUrl - The url sent with first batch of queryAll results to get the next batch

###### Related Salesforce documentation
[queryAllMore](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_queryall.htm)

##### queryMore
If the query results are too large, retrieve the next batch of results

###### Properties
* nextRecordsUrl - The url sent with first batch of query results to get the next batch

###### Related Salesforce documentation
[queryMore](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_query.htm)

##### queryPerformanceFeedback
Get feedback on how Salesforce will execute your query

###### Properties
* queryString - The request SOQL query

###### Related Salesforce documentation
[queryPerformanceFeedback](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_query_explain.htm)

##### createRecord
Creates new records

###### Properties
* sobjectName - The relevant sobject name
* payload - json payload containing record data

###### Related Salesforce documentation
[createRecord](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_sobject_create.htm)

##### createMultipleRecords
Create multiple records

###### Properties
* sobjectName - The relevant sobject name
* payload - json payload containing record data

###### Related Salesforce documentation
[createMultipleRecords](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_composite_sobject_tree_flat.htm)

##### delete
Deletes existing record

###### Properties
* sobjectName - The relevant sobject name

###### Related Salesforce documentation
[delete](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_delete_record.htm)

##### retrieveFieldValues
Retrieve field values from a record

###### Properties
* sobjectName: The relevant sobject name
* rowId: The row ID of the required record
* fields: The comma separated set of required fields

###### Related Salesforce documentation
[retrieveFieldValues](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_get_field_values.htm)

##### retrieveFieldValuesFromExternalObject
Retrieve field values from an external record

###### Properties
* sobjectName: The relevant sobject name
* rowId: The row ID of the required record
* fields: The comma separated set of required fields

###### Related Salesforce documentation
[retrieveFieldValuesFromExternalObject](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_get_field_values_external_object_hdv.htm)

##### retrieveStandardFieldValuesFromExternalObjectWithExternalId
Retrieve field values from an external record with external ID

###### Properties
* sobjectName: The relevant sobject name
* externalId: The row ID of the required external record
* fields: The comma separated set of required fields

###### Related Salesforce documentation
[retrieveStandardFieldValuesFromExternalObjectWithExternalId](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_get_field_values_external_object.htm)

##### update
Updates an existing record

###### Properties
* sobjectName: The relevant sobject name
* payload - json payload containing record data

###### Related Salesforce documentation
[update](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_update_fields.htm)

##### upsert
If record exists, update it else inserts it

###### Properties
* sobjectName: The relevant sobject name
* externalField: The external field id
* fieldValueId: The external field value
* payload - json payload containing record data

###### Related Salesforce documentation
[upsert](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_upsert.htm)


## Running samples

##### Invoke the actions

- Copy `connector-salesforcerest/component/samples/salesforcerest/samples.bal` file and paste it into `<ballerina-tools>/bin` folder.
- Run the following commands to execute the relevant salesforcerest connector action.

###### NOTE
If the template parameter is indicate as optional you must pass null as default value to run this
action.


1. **describeGlobal:**

`bin$ ./ballerina run samples.bal describeGlobal <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion>`

2. **sObjectDescribe:**

`bin$ ./ballerina run samples.bal sObjectDescribe <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance>  <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName>`

3. **listAvailableApiVersion:**

`bin$ ./ballerina run samples.bal listAvailableApiVersion <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath>`

4. **listOrganizationLimits:**

`bin$ ./ballerina run samples.bal listOrganizationLimits <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion>`

5. **listResourcesByApiVersion:**

`bin$ ./ballerina run samples.bal listResourcesByApiVersion <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <requestingApiVersion>`

6. **sObjectBasicInfo:**

`bin$ ./ballerina run samples.bal sObjectBasicInfo <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName>`

7. **sObjectGetDeleted:**

`bin$ ./ballerina run samples.bal sObjectGetDeleted <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <startTime> <endTime>`

8. **sObjectGetUpdated:**

`bin$ ./ballerina run samples.bal sObjectGetUpdated <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <startTime> <endTime>`

9. **sObjectPlatformAction:**

`bin$ ./ballerina run samples.bal sObjectPlatformAction <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion>`

10. **sObjectRows:**

`bin$ ./ballerina run samples.bal sObjectRows <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName> <rowId>`

11. **sObjectRowsByExternalId:**

`bin$ ./ballerina run samples.bal sObjectRowsByExternalId <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName> <fieldId> <fieldValue>`

12. **listviewQueryPerformanceFeedback:**

`bin$ ./ballerina run samples.bal listviewQueryPerformanceFeedback <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <listViewId>`

13. **query:**

`bin$ ./ballerina run samples.bal query <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <queryString>`

14. **queryAll:**

`bin$ ./ballerina run samples.bal queryAll <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <queryString>`

15. **queryAllMore:**

`bin$ ./ballerina run samples.bal queryAllMore <accessToken> <clientID> <clientSecret> <refreshToken <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <nextRecordsUrl>`

16. **queryMore:**

`bin$ ./ballerina run samples.bal queryMore <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint>  <refreshTokenPath> <apiVersion> <nextRecordsUrl>`

17. **queryPerformanceFeedback:**

`bin$ ./ballerina run samples.bal queryPerformanceFeedback <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <queryString>`

18. **createRecord:**

`bin$ ./ballerina run samples.bal createRecord <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion>`

19. **createMultipleRecords:**

`bin$ ./ballerina run samples.bal createMultipleRecords <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion>`

20. **delete:**

`bin$ ./ballerina run samples.bal delete <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion>  <sobjectName> <deleteId>`

21. **retrieveFieldValues:**

`bin$ ./ballerina run samples.bal retrieveFieldValues <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName> <rowId> <fields>`

22. **retrieveFieldValuesFromExternalObject:**

`bin$ ./ballerina run samples.bal retrieveFieldValuesFromExternalObject <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName> <rowId> <fields>`

23. **retrieveStandardFieldValuesFromExternalObjectWithExternalId:**

`bin$ ./ballerina run samples.bal retrieveStandardFieldValuesFromExternalObjectWithExternalId <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName> <externalId> <fields>`

24. **update:**

`bin$ ./ballerina run samples.bal update <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <recordId>`

25. **upsert:**

`bin$ ./ballerina run samples.bal upsert <accessToken> <clientID> <clientSecret> <refreshToken> <apiInstance> <refreshTokenEndpoint> <refreshTokenPath> <apiVersion> <sobjectName> <externalField> <fieldValueId>`

**Note :-**

Here, 

refreshTokenEndpoint - The base url of the refresh token endpoint. Eg: "https://ap4.salesforce.com"

refreshTokenPath - Resource path for refresh token endpoint. Eg: "/services/oauth2/token"



| Ballerina Version | Salesforce REST Connector Version |
| ----------------- | ---------------------- |
| 0.95.3 | 0.95.0 |