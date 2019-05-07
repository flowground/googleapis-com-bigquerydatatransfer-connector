# ![LOGO](logo.png) BigQuery Data Transfer **flow**ground Connector

## Description

A generated **flow**ground connector for the BigQuery Data Transfer API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/bigquerydatatransfer/v1/swagger.json<br/>
Generated at: 2019-05-07T17:41:13+03:00

## API Description

Schedule queries or transfer external data from SaaS applications to Google BigQuery on a regular basis.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Deletes the specified transfer run.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The field will contain name of the resource requested, for example:
`projects/{project_id}/transferConfigs/{config_id}/runs/{run_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns information about the particular transfer run.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The field will contain name of the resource requested, for example:
`projects/{project_id}/transferConfigs/{config_id}/runs/{run_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a data transfer configuration.<br/>
> All fields must be set, even if they are not updated.

*Tags:* `projects`

#### Input Parameters
* `authorizationCode` - _optional_ - Optional OAuth2 authorization code to use with this transfer configuration.
If it is provided, the transfer configuration will be associated with the
authorizing user.
In order to obtain authorization_code, please make a
request to
https://www.gstatic.com/bigquerydatatransfer/oauthz/auth?client_id=<datatransferapiclientid>&scope=<data_source_scopes>&redirect_uri=<redirect_uri>

* client_id should be OAuth client_id of BigQuery DTS API for the given
  data source returned by ListDataSources method.
* data_source_scopes are the scopes returned by ListDataSources method.
* redirect_uri is an optional parameter. If not specified, then
  authorization code is posted to the opener of authorization flow window.
  Otherwise it will be sent to the redirect uri. A special value of
  urn:ietf:wg:oauth:2.0:oob means that authorization code should be
  returned in the title bar of the browser, with the page text prompting
  the user to copy the code and paste it in the application.
* `name` - _required_ - The resource name of the transfer config.
Transfer config names have the form of
`projects/{project_id}/locations/{region}/transferConfigs/{config_id}`.
The name is automatically generated based on the config_id specified in
CreateTransferConfigRequest along with project_id and region. If config_id
is not provided, usually a uuid, even though it is not guaranteed or
required, will be generated for config_id.
* `updateMask` - _optional_ - Required list of fields to be updated in this request.
* `versionInfo` - _optional_ - Optional version info. If users want to find a very recent access token,
that is, immediately after approving access, users have to set the
version_info claim in the token request. To obtain the version_info, users
must use the "none+gsession" response type. which be return a
version_info back in the authorization response which be be put in a JWT
claim in the token request.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists information about the supported locations for this service.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - The standard list filter.
* `name` - _required_ - The resource that owns the locations collection, if applicable.
* `pageSize` - _optional_ - The standard list page size.
* `pageToken` - _optional_ - The standard list page token.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns true if valid credentials exist for the given data source and<br/>
> requesting user.<br/>
> Some data sources doesn't support service account, so we need to talk to<br/>
> them on behalf of the end user. This API just checks whether we have OAuth<br/>
> token for the particular user, which is a pre-requisite before user can<br/>
> create a transfer config.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The data source in the form:
`projects/{project_id}/dataSources/{data_source_id}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists supported data sources and returns their settings,<br/>
> which can be used for UI rendering.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Page size. The default page size is the maximum value of 1000 results.
* `pageToken` - _optional_ - Pagination token, which can be used to request a specific page
of `ListDataSourcesRequest` list results. For multiple-page
results, `ListDataSourcesResponse` outputs
a `next_page` token, which can be used as the
`page_token` value to request the next page of list results.
* `parent` - _required_ - The BigQuery project id for which data sources should be returned.
Must be in the form: `projects/{project_id}`
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns information about running and completed jobs.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Page size. The default page size is the maximum value of 1000 results.
* `pageToken` - _optional_ - Pagination token, which can be used to request a specific page
of `ListTransferRunsRequest` list results. For multiple-page
results, `ListTransferRunsResponse` outputs
a `next_page` token, which can be used as the
`page_token` value to request the next page of list results.
* `parent` - _required_ - Name of transfer configuration for which transfer runs should be retrieved.
Format of transfer configuration resource name is:
`projects/{project_id}/transferConfigs/{config_id}`.
* `runAttempt` - _optional_ - Indicates how run attempts are to be pulled.
    Possible values: RUN_ATTEMPT_UNSPECIFIED, LATEST.
* `states` - _optional_ - When specified, only transfer runs with requested states are returned.
    Possible values: RUN_ATTEMPT_UNSPECIFIED, LATEST.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns information about all data transfers in the project.

*Tags:* `projects`

#### Input Parameters
* `dataSourceIds` - _optional_ - When specified, only configurations of requested data sources are returned.
* `pageSize` - _optional_ - Page size. The default page size is the maximum value of 1000 results.
* `pageToken` - _optional_ - Pagination token, which can be used to request a specific page
of `ListTransfersRequest` list results. For multiple-page
results, `ListTransfersResponse` outputs
a `next_page` token, which can be used as the
`page_token` value to request the next page of list results.
* `parent` - _required_ - The BigQuery project id for which data sources
should be returned: `projects/{project_id}`.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a new data transfer configuration.

*Tags:* `projects`

#### Input Parameters
* `authorizationCode` - _optional_ - Optional OAuth2 authorization code to use with this transfer configuration.
This is required if new credentials are needed, as indicated by
`CheckValidCreds`.
In order to obtain authorization_code, please make a
request to
https://www.gstatic.com/bigquerydatatransfer/oauthz/auth?client_id=<datatransferapiclientid>&scope=<data_source_scopes>&redirect_uri=<redirect_uri>

* client_id should be OAuth client_id of BigQuery DTS API for the given
  data source returned by ListDataSources method.
* data_source_scopes are the scopes returned by ListDataSources method.
* redirect_uri is an optional parameter. If not specified, then
  authorization code is posted to the opener of authorization flow window.
  Otherwise it will be sent to the redirect uri. A special value of
  urn:ietf:wg:oauth:2.0:oob means that authorization code should be
  returned in the title bar of the browser, with the page text prompting
  the user to copy the code and paste it in the application.
* `parent` - _required_ - The BigQuery project id where the transfer configuration should be created.
Must be in the format projects/{project_id}/locations/{location_id}
If specified location and location of the destination bigquery dataset
do not match - the request will fail.
* `versionInfo` - _optional_ - Optional version info. If users want to find a very recent access token,
that is, immediately after approving access, users have to set the
version_info claim in the token request. To obtain the version_info, users
must use the "none+gsession" response type. which be return a
version_info back in the authorization response which be be put in a JWT
claim in the token request.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns user facing log messages for the data transfer run.

*Tags:* `projects`

#### Input Parameters
* `messageTypes` - _optional_ - Message types to return. If not populated - INFO, WARNING and ERROR
messages are returned.
* `pageSize` - _optional_ - Page size. The default page size is the maximum value of 1000 results.
* `pageToken` - _optional_ - Pagination token, which can be used to request a specific page
of `ListTransferLogsRequest` list results. For multiple-page
results, `ListTransferLogsResponse` outputs
a `next_page` token, which can be used as the
`page_token` value to request the next page of list results.
* `parent` - _required_ - Transfer run name in the form:
`projects/{project_id}/transferConfigs/{config_Id}/runs/{run_id}`.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates transfer runs for a time range [start_time, end_time].<br/>
> For each date - or whatever granularity the data source supports - in the<br/>
> range, one transfer run is created.<br/>
> Note that runs are created per UTC time in the time range.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - Transfer configuration name in the form:
`projects/{project_id}/transferConfigs/{config_id}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-bigquerydatatransfer-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
