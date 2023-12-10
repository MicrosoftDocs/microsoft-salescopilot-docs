---
title: Sample OpenAPI definition (preview)
description: Sample OpenAPI definition for the API implementation.
ms.date: 12/11/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
  - ai-gen-title
---

# Sample OpenAPI definition (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

Refer to the following guidelines when creating the OpenAPI definition for the API implementation.

- The OpenAPI definition contains placeholders for the actual API paths. You can replace the placeholders with the actual API paths. The actual OpenAPI definition provided by the connector is used and requests are built based on the API paths in the OpenAPI definition.
- HTTP methods should be same as the ones specified in the OpenAPI definition.
- Input parameter names should be the same as the ones specified in the OpenAPI definition. OpenAPI definition returned by the connector is used to map the input parameters by names. All the required input parameters in the sample OpenAPI definition must be present in the actual connector definition.
- Input parameter types should be same as the ones specified in the OpenAPI definition. 
- Operation IDs should be same as the ones specified in the OpenAPI definition. Every operation described by the OpenAPI definition must have a unique identifier. APIs are invoked based on the operation IDs.
- APIs described by the OpenAPI definition should not contain any additional required parameters that are not present in the sample OpenAPI definition. If there are any additional required parameters, Copilot for Sales won't invoke the APIs and will fail with an internal error.
- Properties of output objects that are marked as required in the OpenAPI definition must be present in the API response.
- Include the following internal properties. It helps Power Platform to do the required processing:
    - x-ms-keywords 
    - x-ms-openai-data 

## OpenAPI definition

You can use the following sample OpenAPI definition as a reference.

```json
 
{ 

  "swagger": "2.0", 

  "info": { 

    "title": "<sample title>", 

    "version": "1.0", 

    "x-ms-keywords": "<your keywords of connector name go here>" 

  }, 

  "paths": { 

    "<your API path goes here>": { 

      "get": { 

        "tags": [ 

          "Documents" 

        ], 

        "operationId": "scp-get-related-activities", 

        "produces": [ 

          "application/json" 

        ], 

        "parameters": [ 

          { 

            "in": "query", 

            "name": "recordType", 

            "required": true, 

            "type": "string", 

            "enum": [ 

              "account", 

              "opportunity" 

            ] 

          }, 

          { 

            "in": "query", 

            "name": "recordId", 

            "required": true, 

            "type": "string" 

          }, 

          { 

            "in": "query", 

            "name": "startDateTime", 

            "type": "string", 

            "format": "date-time" 

          }, 

          { 

            "in": "query", 

            "name": "endDateTime", 

            "type": "string", 

            "format": "date-time" 

          }, 

          { 

            "in": "query", 

            "name": "top", 

            "type": "integer", 

            "format": "int32" 

          }, 

          { 

            "in": "query", 

            "name": "skip", 

            "type": "integer", 

            "format": "int32" 

          }, 

          { 

            "in": "query", 

            "name": "crmType", 

            "type": "string", 

            "enum": [ 

              "Salesforce", 

              "Dynamics365" 

            ] 

          }, 

          { 

            "in": "query", 

            "name": "crmOrgUrl", 

            "type": "string" 

          } 

        ], 

        "responses": { 

          "200": { 

            "description": "Success", 

            "schema": { 

              "$ref": "#/definitions/ActivityListResponseEnvelope" 

            } 

          }, 

          "400": { 

            "description": "Bad Request", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "401": { 

            "description": "Unauthorized", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "403": { 

            "description": "Forbidden", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "404": { 

            "description": "Not Found", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "429": { 

            "description": "Too Many Requests", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "500": { 

            "description": "Server Error", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          } 

        }, 

        "x-ms-openai-data": { 

          "openai-enabled": true 

        } 

      } 

    }, 

    "<your API path goes here>": { 

      "get": { 

        "tags": [ 

          "Documents" 

        ], 

        "operationId": "scp-get-related-records", 

        "produces": [ 

          "application/json" 

        ], 

        "parameters": [ 

          { 

            "in": "query", 

            "name": "recordType", 

            "required": true, 

            "type": "string", 

            "enum": [ 

              "account", 

              "opportunity" 

            ] 

          }, 

          { 

            "in": "query", 

            "name": "recordId", 

            "required": true, 

            "type": "string" 

          }, 

          { 

            "in": "query", 

            "name": "top", 

            "type": "integer", 

            "format": "int32" 

          }, 

          { 

            "in": "query", 

            "name": "skip", 

            "type": "integer", 

            "format": "int32" 

          }, 

          { 

            "in": "query", 

            "name": "crmType", 

            "type": "string", 

            "enum": [ 

              "Salesforce", 

              "Dynamics365" 

            ] 

          }, 

          { 

            "in": "query", 

            "name": "crmOrgUrl", 

            "type": "string" 

          } 

        ], 

        "responses": { 

          "200": { 

            "description": "Success", 

            "schema": { 

              "$ref": "#/definitions/DocumentRecordListResponseEnvelope" 

            } 

          }, 

          "400": { 

            "description": "Bad Request", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "401": { 

            "description": "Unauthorized", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "403": { 

            "description": "Forbidden", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "404": { 

            "description": "Not Found", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "429": { 

            "description": "Too Many Requests", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          }, 

          "500": { 

            "description": "Server Error", 

            "schema": { 

              "$ref": "#/definitions/ApiError" 

            } 

          } 

        }, 

        "x-ms-openai-data": { 

          "openai-enabled": true 

        } 

      } 

    } 

  }, 

  "definitions": { 

    "Activity": { 

      "required": [ 

        "dateTime", 

        "description", 

        "title" 

      ], 

      "type": "object", 

      "properties": { 

        "title": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "description": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "dateTime": { 

          "format": "date-time", 

          "type": "string" 

        }, 

        "url": { 

          "type": "string" 

        }, 

        "additionalProperties": { 

          "type": "object", 

          "additionalProperties": { 

            "type": "string" 

          } 

        } 

      } 

    }, 

    "ActivityListResponseEnvelope": { 

      "type": "object", 

      "properties": { 

        "value": { 

          "type": "array", 

          "items": { 

            "$ref": "#/definitions/Activity" 

          } 

        }, 

        "hasMoreResults": { 

          "type": "boolean" 

        } 

      } 

    }, 

    "ApiError": { 

      "required": [ 

        "errorCode" 

      ], 

      "type": "object", 

      "properties": { 

        "errorCode": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "errorMessage": { 

          "type": "string" 

        }, 

        "activityId": { 

          "type": "string" 

        }, 

        "details": { 

          "type": "object", 

          "additionalProperties": {} 

        } 

      } 

    }, 

    "DocumentRecord": { 

      "required": [ 

        "recordId", 

        "recordTitle", 

        "recordType", 

        "recordTypeDisplayName", 

        "recordTypePluralDisplayName" 

      ], 

      "type": "object", 

      "properties": { 

        "recordId": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "recordTypeDisplayName": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "recordTitle": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "recordTypePluralDisplayName": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "recordType": { 

          "minLength": 1, 

          "type": "string" 

        }, 

        "url": { 

          "type": "string" 

        }, 

        "additionalProperties": { 

          "type": "object", 

          "additionalProperties": { 

            "type": "string" 

          } 

        } 

      } 

    }, 

    "DocumentRecordListResponseEnvelope": { 

      "type": "object", 

      "properties": { 

        "value": { 

          "type": "array", 

          "items": { 

            "$ref": "#/definitions/DocumentRecord" 

          } 

        }, 

        "hasMoreResults": { 

          "type": "boolean" 

        } 

      } 

    } 

  } 

} 
```