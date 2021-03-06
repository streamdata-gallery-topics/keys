---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get comment property
  description: Returns the value of the property with a given key from the comment
    identified by the key or by the id. The user who retrieves the property is required
    to have permissions to read the comment.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/comment/{commentId}/properties:
    get:
      summary: Get comment property keys
      description: Returns the keys of all properties for the comment identified by
        the key or by the id.
      operationId: com.atlassian.jira.rest.v2.issue.CommentPropertyResource.getCommentPropertyKeys_get
      x-api-path-slug: api2commentcommentidproperties-get
      parameters:
      - in: path
        name: commentId
        description: the comment from which keys will be returned
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Property
      - Keys
  /api/2/dashboard/{dashboardId}/items/{itemId}/properties:
    get:
      summary: Get dashboard item property keys
      description: "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to get the property keys the
        user must be the owner of the dashboard or be shared the dashboard. Note,
        users with the _Administer Jira_ [global permission](href=) are considered
        owners of the System dashboard. The System dashboard is considered to be shared
        with all other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemPropertyKeys_get
      x-api-path-slug: api2dashboarddashboardiditemsitemidproperties-get
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
      - Keys
  /api/2/issue/{issueIdOrKey}/properties:
    get:
      summary: Get issue property keys
      description: Returns the keys of all properties for the issue identified by
        the key or by the id.
      operationId: com.atlassian.jira.rest.v2.issue.IssuePropertyResource.getIssuePropertyKeys_get
      x-api-path-slug: api2issueissueidorkeyproperties-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: the issue from which keys will be returned
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Property
      - Keys
  /api/2/issue/{issueIdOrKey}/worklog/{worklogId}/properties:
    get:
      summary: Get worklog property keys
      description: Returns the keys of all properties for the worklog identified by
        the key or by the id.
      operationId: com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.getWorklogPropertyKeys_get
      x-api-path-slug: api2issueissueidorkeyworklogworklogidproperties-get
      parameters:
      - in: path
        name: issueIdOrKey
      - in: path
        name: worklogId
        description: the worklog from which keys will be returned
      responses:
        200:
          description: OK
      tags:
      - Worklog
      - Property
      - Keys
  /api/2/issuetype/{issueTypeId}/properties:
    get:
      summary: Get issue type property keys
      description: |-
        Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.
        *   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypePropertyKeys_get
      x-api-path-slug: api2issuetypeissuetypeidproperties-get
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
      - Keys
  /api/2/project/{projectIdOrKey}/properties:
    get:
      summary: Get project property keys
      description: |-
        Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectPropertyKeys_get
      x-api-path-slug: api2projectprojectidorkeyproperties-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
      - Keys
  /api/2/user/properties:
    get:
      summary: Get user property keys
      description: |-
        Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To access the calling user's property keys: None

        Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
      operationId: com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.getUserPropertyKeys_get
      x-api-path-slug: api2userproperties-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: query
        name: userKey
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Property
      - Keys
  /api/2/user/search/query/key:
    get:
      summary: Find user keys by query
      description: |-
        Finds users using a structured query and returns a list of user keys. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available query statements are:

        *   `is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.
        *   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.
        *   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.
        *   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.
        *   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.
        *   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.
        *   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.
        *   `[propertyKey].entity.property.path is "property value"` Returns users with the entity property value.

        The list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:

        `is assignee of PROJ AND [propertyKey].entity.property.path is "property value"`
      operationId: com.atlassian.jira.rest.v2.search.UserSearchResource.findUserKeysByQuery_get
      x-api-path-slug: api2usersearchquerykey-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: includeInactive
        description: Include inactive users in the results
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: query
        description: The search query
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Find
      - User
      - Keys
      - By
      - Query
  /api/2/project/type/{projectTypeKey}:
    get:
      summary: Get project type by key
      description: |-
        Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getProjectTypeByKey_get
      x-api-path-slug: api2projecttypeprojecttypekey-get
      parameters:
      - in: path
        name: projectTypeKey
        description: The key of the project type
      responses:
        200:
          description: OK
      tags:
      - Project
      - Type
      - By
      - Key
  /api/2/project/type/{projectTypeKey}/accessible:
    get:
      summary: Get accessible project type by key
      description: |-
        Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAccessibleProjectTypeByKey_get
      x-api-path-slug: api2projecttypeprojecttypekeyaccessible-get
      parameters:
      - in: path
        name: projectTypeKey
        description: The key of the project type
      responses:
        200:
          description: OK
      tags:
      - Accessible
      - Project
      - Type
      - By
      - Key
  /api/2/projectvalidate/key:
    get:
      summary: Validate project key
      description: Validates a project key.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectValidateResource.validateProjectKey_get
      x-api-path-slug: api2projectvalidatekey-get
      parameters:
      - in: query
        name: key
        description: the project key
      responses:
        200:
          description: OK
      tags:
      - Validate
      - Project
      - Key
  /api/2/projectvalidate/validProjectKey:
    get:
      summary: Get valid project key
      description: Validates the project key and generated a valid project key if
        the supplied key is invalid.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectValidateResource.getValidProjectKey_get
      x-api-path-slug: api2projectvalidatevalidprojectkey-get
      parameters:
      - in: query
        name: key
        description: the project key
      responses:
        200:
          description: OK
      tags:
      - Valid
      - Project
      - Key
  /api/2/comment/{commentId}/properties/{propertyKey}:
    get:
      summary: Get comment property
      description: Returns the value of the property with a given key from the comment
        identified by the key or by the id. The user who retrieves the property is
        required to have permissions to read the comment.
      operationId: com.atlassian.jira.rest.v2.issue.CommentPropertyResource.getCommentProperty_get
      x-api-path-slug: api2commentcommentidpropertiespropertykey-get
      parameters:
      - in: path
        name: commentId
        description: the comment from which the property will be returned
      - in: path
        name: propertyKey
        description: the key of the property to return
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Property
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---