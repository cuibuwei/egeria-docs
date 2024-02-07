<!-- SPDX-License-Identifier: CC-BY-4.0 -->
<!-- Copyright Contributors to the Egeria project. -->

## Configure the basic properties

The basic properties are used in logging and events originating from the server. They help to document the purpose of the server (which helps with problem determination) and enable performance improvements by allowing the server to ignore activity or metadata that is not relevant to its operation.

The basic properties include two unique identifiers that are set up when you first create the configuration document:

| Property          | Description |
|-------------------|---|
| *localServerId*   | Unique identifier for this server. By default, this is initialized to a randomly generated Universal Unique identifier (UUID). |
| *localServerName* | Meaningful name for the server for use in messages and UIs. Ideally this value is unique to aid administrators in understanding the source of messages and events from the server. This value is set to the server name assigned when the configuration is created. |

The other basic properties have values that can be changed through the admin services API:

| Property                 | Description                                                                                                                                                                                                                                                                                                                           |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *localServerDescription* | Description for the server. This is useful information for the administrator to understand the role of the server. The default value is `null`.                                                                                                                                                                                       |
| *organizationName*       | Descriptive name for the organization that owns the local server/repository. This is useful when the open metadata repository cluster consists of metadata servers from different organizations, or different departments of an enterprise. The default value is `null`.                                                              |
| *localServerUserId*      | UserId to use for server-initiated REST calls. The default is `OMAGServer`.                                                                                                                                                                                                                                                           |
| *localServerPassword*    | Password to use for server-initiated REST calls. The default is `null`. This means that only the userId is sent in the HTTP header.                                                                                                                                                                                                   |
| *localServerType*        | Descriptive type name for the server. Again this is useful information for the administrator to understand the role of the server. The default value is `null` which means that the [server operation services](/services/server-operations) will populate it automatically based on the services that are configured for the server. |
| *maxPageSize*            | The maximum page size that can be set on requests to the server. The default value is `1000`. A value of zero means unlimited page size. Although supported, the zero value is not recommended because it provides no protection from a large request denial of service attack.                                                       |

The sections that follow cover how to set up these values.

### Set basic server properties

The server type name should be set to something that describes the OMAG Server's role. It may be the name of a specific product that it is enabling, or a role in the metadata and governance landscape.  The default value is `Open Metadata and Governance Server`.

If you have no specific value to set the server type name to, we recommend that you set the server type name to null.  This will cause the server start up process will derive a standard server type name based on the rest of the configuration for the server.

???+ post "POST - setBasicServerProperties"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/server-properties"
    ```
    The request body contains the properties to set.
    
    | Property                 | Description                                                                                                                                                                                                                                                                     |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | *localServerDescription* | Description for the server. This is useful information for the administrator to understand the role of the server. The default value is `null`.                                                                                                                                 |
    | *organizationName*       | Descriptive name for the organization that owns the local server/repository. This is useful when the open metadata repository cluster consists of metadata servers from different organizations, or different departments of an enterprise. The default value is `null`.        |
    | *localServerURL*         | The *platformURLRoot* for the platform where this server is to run. For example `https://localhost:9443`.  It is used if the server connects to a [cohort](/concepts/cohort-member).                                                                                            |
    | *localServerUserId*      | UserId to use for server-initiated REST calls. The default is `OMAGServer`.                                                                                                                                                                                                     |
    | *localServerPassword*    | Password to use for server-initiated REST calls. The default is `null`. This means that only the userId is sent in the HTTP header.                                                                                                                                             |
    | *maxPageSize*            | The maximum page size that can be set on requests to the server. The default value is `1000`. A value of zero means unlimited page size. Although supported, the zero value is not recommended because it provides no protection from a large request denial of service attack. |
    
    For example:
    
    ```json
    {
      "localServerDescription" : "This server supports the governance teams",
      "organizationName" : "Coco Pharmaceuticals",
      "localServerURL" : "https://localhost:9443",
      "localServerUserId" : "cocomds2npa",
      "localServerPassword" : "secret",
      "maxPageSize" : 600
    }
    ```
     
Alternatively, you can set these properties one at a time.

### Set server description

The server description should be set to something that describes the OMAG Server's role. It may be the name of a specific product that it is enabling, or a role in the metadata and governance landscape.  Its purpose is to help administrators identify which server configuration they need to work with.

!!! post "POST - setServerDescription"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/server-description"
    ```
The description is passed in the request body as a text string.

### Set organization name

The organization name may be the owning organization or you may use it to identify the department or team that is supported by this server.

!!! post "POST - setOrganizationName"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/organization-name?name="{{organizationName}}"
    ```

### Set the server's userId and optional password

The server's userId is used when processing requests that do not have an end user, such as receiving an event from a topic. The default value is `OMAGServer`. Ideally each server should have its own userId, so it is possible to restrict the resources that each server has access to and identify the origin of updates to the metadata elements.

If the password is specified as well, the userId and password combination are used to provide authentication information on each REST call made by the server.

!!! post "POST - setServerUserId"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/server-user-id?id="{{serverUserId}}"
    ```

!!! post "POST - setServerPassword"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/server-user-password?password="{{serverUserPassword}}"
    ```

### Set the maximum page size for REST API requests

The maximum page size value sets an upper limit on the number of results that a caller can request on any paging REST API to this server. Setting maximum page size helps to prevent a denial of service attack that uses very large requests to overwhelm the server. A value of `0` means no limit, and leaves the server open to such attacks.

!!! post "POST - setMaxPageSize"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/max-page-size?limit={{maxPageSize}}
    ```

### Set server type name

Typically, the server type name should be left blank to allow the [server operations service](/services/server-operations) to classify the server from its configuration, since it gives the servers standard type values.

If, however, you want to use your own values, then this is the command to set it up.

!!! post "POST - setDescriptiveServerType"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/server-type?typeName="{{serverTypeName}}"
    ```

### Get server type classification

If you are curious to see the automated server type that has been assigned to a server, it can be retrieved with the following command.

!!! get "GET - getServerClassification"
    ```
    {{platformURLRoot}}/open-metadata/admin-services/users/{{adminUserId}}/servers/{{serverName}}/server-type-classification"
    ```