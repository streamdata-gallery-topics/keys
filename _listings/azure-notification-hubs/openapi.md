---
swagger: "2.0"
x-collection-name: Azure Notification Hubs
x-complete: 1
info:
  title: NotificationHubsManagementClient
  description: azure-notificationhub-client
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/listKeys
  : post:
      summary: Namespaces List Keys
      description: Gets the Primary and Secondary ConnectionStrings to the namespace
      operationId: Namespaces_ListKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulenamelistkeys-post
      parameters:
      - in: path
        name: authorizationRuleName
        description: The connection string of the namespace for the specified authorizationRule
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/regenerateKeys
  : post:
      summary: Namespaces Regenerate Keys
      description: Regenerates the Primary/Secondary Keys to the Namespace Authorization
        Rule
      operationId: Namespaces_RegenerateKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulenameregeneratekeys-post
      parameters:
      - in: path
        name: authorizationRuleName
        description: The connection string of the namespace for the specified authorizationRule
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to regenerate the Namespace Authorization
          Rule Key
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Regenerate Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/notificationHubs/{notificationHubName}/AuthorizationRules/{authorizationRuleName}/listKeys
  : post:
      summary: Notification Hubs List Keys
      description: Gets the Primary and Secondary ConnectionStrings to the NotificationHub
      operationId: NotificationHubs_ListKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenamenotificationhubsnotificationhubnameauthorizationrulesauthorizationrulenamelistkeys-post
      parameters:
      - in: path
        name: authorizationRuleName
        description: The connection string of the NotificationHub for the specified
          authorizationRule
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: notificationHubName
        description: The notification hub name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Notification Hubs Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/notificationHubs/{notificationHubName}/AuthorizationRules/{authorizationRuleName}/regenerateKeys
  : post:
      summary: Notification Hubs Regenerate Keys
      description: Regenerates the Primary/Secondary Keys to the NotificationHub Authorization
        Rule
      operationId: NotificationHubs_RegenerateKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenamenotificationhubsnotificationhubnameauthorizationrulesauthorizationrulenameregeneratekeys-post
      parameters:
      - in: path
        name: authorizationRuleName
        description: The connection string of the NotificationHub for the specified
          authorizationRule
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: notificationHubName
        description: The notification hub name
      - in: body
        name: parameters
        description: Parameters supplied to regenerate the NotificationHub Authorization
          Rule Key
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Notification Hubs Regenerate Keys
---