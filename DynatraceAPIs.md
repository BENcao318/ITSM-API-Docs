### Dynatrace API
#### - This site require creating access token with proper scopes inside the Dynatrace app in order to access the specific APIs. 
#### -  {{domain}} in the following URLs indicates the app you created on Dynatrace (e.g. abg27873.apps.dynatrace.com)

1. GET entities list
   - Example cURL:
   ```
    https://{{domain}}/api/v2/entities?entitySelector=type(%22SERVICE%22),mzId(%229130632296508575249%22)&fields=lastSeenTms,properties.serviceTechnologyTypes
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "totalCount": 52,
        "pageSize": 50,
        "nextPageKey": "AQArdHlwZSgiU0VSVklDRSIpL",
        "entities": [
            {
            "entityId": "SERVICE-1125C375A187D27A",
            "displayName": "dotNetBackend_easyTravel_x64",
            "lastSeenTms": 1590609632865,
            "properties": {
                "serviceTechnologyTypes": [
                "IIS app pool",
                "ASP.NET",
                "DotNet"
                ]
            }
            },
            {
            "entityId": "SERVICE-42C0B06C4DCFD0EF",
            "displayName": "AuthenticationService",
            "lastSeenTms": 1590747000977,
            "properties": {
                "serviceTechnologyTypes": [
                "Java"
                ]
            }
            },
            {
            "entityId": "SERVICE-620517BB99A7ED9E",
            "displayName": "BookingService",
            "lastSeenTms": 1590747028702,
            "properties": {
                "serviceTechnologyTypes": [
                "Java"
                ]
            }
            }
        ]
    }
    ```

2. GET all entity types
   - Example cURL:
   ```
    https://{{domain}}/api/v2/entityTypes
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "totalCount": 33,
        "pageSize": 33,
        "types": [
            {
            "type": "APPLICATION",
            "properties": [
                {
                "id": "applicationType",
                "type": "Enum"
                },
                {
                "id": "conditionalName",
                "type": "String"
                },
                {
                "id": "customizedName",
                "type": "String"
                }
            ],
            "tags": "List",
            "managementZones": "List",
            "fromRelationships": [
                {
                "id": "calls",
                "toTypes": [
                    "SERVICE"
                ]
                }
            ],
            "toRelationships": []
            },
            {
            "type": "HOST",
            "properties": [
                {
                "id": "ipAddresses",
                "type": "List"
                },
                {
                "id": "osType",
                "type": "Enum"
                },
                {
                "id": "osVersion",
                "type": "String"
                }
            ],
            "tags": "List",
            "managementZones": "List",
            "fromRelationships": [
                {
                "id": "runsOn",
                "toTypes": [
                    "EC2_INSTANCE",
                    "VIRTUALMACHINE",
                    "AZURE_VM",
                    "OPENSTACK_VM",
                    "GOOGLE_COMPUTE_ENGINE",
                    "HYPERVISOR"
                ]
                },
                {
                "id": "runsOnResource",
                "toTypes": [
                    "CUSTOM_DEVICE"
                ]
                },
                {
                "id": "isInstanceOf",
                "toTypes": [
                    "HOST_GROUP"
                ]
                },
                {
                "id": "isNetworkClientOfHost",
                "toTypes": [
                    "HOST",
                    "CUSTOM_DEVICE"
                ]
                },
                {
                "id": "candidateTalksWith",
                "toTypes": [
                    "CUSTOM_DEVICE",
                    "PROCESS_GROUP_INSTANCE"
                ]
                }
            ],
            "toRelationships": [
                {
                "id": "isProcessOf",
                "fromTypes": [
                    "PROCESS_GROUP_INSTANCE"
                ]
                },
                {
                "id": "runsOn",
                "fromTypes": [
                    "OPENSTACK_VM",
                    "PROCESS_GROUP"
                ]
                },
                {
                "id": "isSiteOf",
                "fromTypes": [
                    "GEOLOC_SITE",
                    "VMWARE_DATACENTER"
                ]
                },
                {
                "id": "talksWithCandidate",
                "fromTypes": [
                    "CUSTOM_DEVICE",
                    "PROCESS_GROUP_INSTANCE"
                ]
                },
                {
                "id": "isNetworkClientOfHost",
                "fromTypes": [
                    "CUSTOM_DEVICE",
                    "HOST"
                ]
                },
                {
                "id": "isDiskOf",
                "fromTypes": [
                    "DISK"
                ]
                },
                {
                "id": "runsOnHost",
                "fromTypes": [
                    "SERVICE"
                ]
                },
                {
                "id": "isContainerGroupInstanceOfHost",
                "fromTypes": [
                    "CONTAINER_GROUP_INSTANCE"
                ]
                }
            ]
            },
            {
            "type": "SERVICE",
            "properties": [
                {
                "id": "mainServiceSoftwareTech",
                "type": "Map"
                },
                {
                "id": "port",
                "type": "Number"
                },
                {
                "id": "serviceType",
                "type": "Enum"
                }
            ],
            "tags": "List",
            "managementZones": "List",
            "fromRelationships": [
                {
                "id": "runsOn",
                "toTypes": [
                    "CUSTOM_DEVICE_GROUP",
                    "PROCESS_GROUP"
                ]
                },
                {
                "id": "runsOnProcessGroupInstance",
                "toTypes": [
                    "CUSTOM_DEVICE",
                    "PROCESS_GROUP_INSTANCE"
                ]
                },
                {
                "id": "runsOnHost",
                "toTypes": [
                    "CUSTOM_DEVICE",
                    "HOST"
                ]
                },
                {
                "id": "calls",
                "toTypes": [
                    "SERVICE"
                ]
                }
            ],
            "toRelationships": [
                {
                "id": "calls",
                "fromTypes": [
                    "MOBILE_APPLICATION",
                    "CUSTOM_APPLICATION",
                    "HTTP_CHECK",
                    "APPLICATION",
                    "SERVICE"
                ]
                }
            ]
            }
        ]
    }
    ```
3. GET problems list
   - Example cURL:
    ```
    https://{{domain}}/api/v2/entityTypes
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "totalCount": 0,
        "pageSize": 50,
        "problems": [],
        "warnings": []
    }
    ```
4. GET all Synthetic monitors
    - Example cURL:
    ```
    https://{{domain}}/api/v1/synthetic/monitors
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "monitors": [
            {
            "name": "easyTravel Angular",
            "entityId": "SYNTHETIC_TEST-000000000000C69F"
            },
            {
            "name": "dynatrace.com",
            "entityId": "SYNTHETIC_TEST-0000000000025434"
            },
            {
            "name": "easytravel special offers",
            "entityId": "SYNTHETIC_TEST-000000000000987A"
            }
        ]
    }
    ```
5. GET all Synthetic locations
    - Example cURL:
    ```
    https://{{domain}}/api/v1/synthetic/locations
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "locations": [
            {
            "name": "Amazon US East (N. Virginia)",
            "entityId": "GEOLOCATION-95196F3C9A4F4215",
            "type": "PUBLIC",
            "cloudPlatform": "AMAZON_EC2",
            "ips": [
                "134.189.153.97",
                "134.189.153.98",
                "134.189.153.99"
            ]
            },
            {
            "name": "AWS Europe (London)",
            "entityId": "GEOLOCATION-A9022AAFA0763F56",
            "type": "PUBLIC",
            "cloudPlatform": "AMAZON_EC2",
            "ips": [
                "243.22.221.174",
                "104.179.71.29"
            ]
            },
            {
            "name": "Gdansk HTTP",
            "entityId": "SYNTHETIC_LOCATION-9C75B59442498323",
            "type": "PRIVATE"
            }
        ]
    }
    ```
6. Get all dashboards
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/dashboard
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
   ```
   {
    "dashboards": [
            {
            "author_handle": "string",
            "created_at": "2019-09-19T10:00:00.000Z",
            "description": "string",
            "id": "string",
            "is_read_only": false,
            "layout_type": "ordered",
            "modified_at": "2019-09-19T10:00:00.000Z",
            "title": "string",
            "url": "string"
            }
        ]
    }
   ```
7. GET metrics
   - Example cURL:
   ```
    https://{{domain}}/api/v2/metrics?fields=unit,aggregationTypes&metricSelector=builtin:*
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
  ```
    {
        "totalCount": 1808,
        "nextPageKey": "___a7acX3q0AAAAGAQAJYnVpbHRpbjoqAQA",
        "metrics": [
            {
            "metricId": "builtin:host.cpu.idle",
            "unit": "Percent",
            "aggregationTypes": [
                "auto",
                "avg",
                "max",
                "min"
            ]
            },
            {
            "metricId": "builtin:host.cpu.load",
            "unit": "Ratio",
            "aggregationTypes": [
                "auto",
                "avg",
                "max",
                "min"
            ]
            },
            {
            "metricId": "builtin:service.errors.server.count",
            "unit": "Count",
            "aggregationTypes": [
                "auto",
                "value"
            ]
            },
            {
            "metricId": "builtin:service.keyRequest.count.client",
            "unit": "Count",
            "aggregationTypes": [
                "auto",
                "value"
            ]
            }
        ]
    }
  ```
8. GET metric descriptor
   - Example cURL:
   ```
    https://{{domain}}/api/v2/metrics/builtin:host.disk.avail
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response 
    ```
    {
        "metricId": "builtin:host.disk.avail",
        "displayName": "Disk available",
        "description": "Amount of free space available for user in file system. On Linux and AIX it is free space available for unprivileged user. It doesn't contain part of free space reserved for the root.",
        "unit": "Byte",
        "dduBillable": false,
        "billable": false,
        "created": 0,
        "lastWritten": null,
        "entityType": [
            "HOST"
        ],
        "aggregationTypes": [
            "auto",
            "avg",
            "max",
            "min"
        ],
        "transformations": [
            "filter",
            "fold",
            "limit",
            "merge",
            "names",
            "parents",
            "timeshift",
            "sort",
            "last",
            "splitBy",
            "lastReal",
            "partition",
            "setUnit"
        ],
        "defaultAggregation": {
            "type": "avg"
        },
        "dimensionDefinitions": [
            {
                "key": "dt.entity.host",
                "name": "Host",
                "displayName": "Host",
                "index": 0,
                "type": "ENTITY"
            },
            {
                "key": "dt.entity.disk",
                "name": "Disk",
                "displayName": "Disk",
                "index": 1,
                "type": "ENTITY"
            }
        ],
        "tags": [],
        "metricValueType": {
            "type": "score"
        },
        "minimumValue": 0.0,
        "scalar": false,
        "resolutionInfSupported": true,
        "unitDisplayFormat": "binary",
        "exported": true
    }
    ```
9.  GET metric data points
    - Example cURL:
   ```
    https://{{domain}}/api/v2/metrics/query?metricSelector=builtin:host.cpu.(usage,idle)&entitySelector=type(%22dt.entity.host%22),entityId(%22HOST-0990886B7D39FE29%22,%22HOST-0956C3557E9109C1%22)&from=now-5m
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "totalCount": 2,
        "nextPageKey": null,
        "result": [
            {
            "metricId": "builtin:host.cpu.idle",
            "dataPointCountRatio": 1.8E-5,
            "dimensionCountRatio": 3.0E-5,
            "data": [
                {
                "dimensions": [
                    "HOST-0990886B7D39FE29"
                ],
                "dimensionMap": {
                    "dt.entity.host": "HOST-0990886B7D39FE29"
                },
                "timestamps": [
                    1589456100000,
                    1589456160000,
                    1589456220000
                ],
                "values": [
                    81.0,
                    81.0,
                    79.0
                ]
                },
                {
                "dimensions": [
                    "HOST-0956C3557E9109C1"
                ],
                "dimensionMap": {
                    "dt.entity.host": "HOST-0956C3557E9109C1"
                },
                "timestamps": [
                    1589456100000,
                    1589456160000,
                    1589456220000
                ],
                "values": [
                    81.0,
                    79.0,
                    78.0
                ]
                }
            ]
            },
            {
            "metricId": "builtin:host.cpu.usage",
            "dataPointCountRatio": 1.8E-5,
            "dimensionCountRatio": 3.0E-5,
            "data": [
                {
                "dimensions": [
                    "HOST-0990886B7D39FE29"
                ],
                "dimensionMap": {
                    "dt.entity.host": "HOST-0990886B7D39FE29"
                },
                "timestamps": [
                    1589456100000,
                    1589456160000,
                    1589456220000
                ],
                "values": [
                    19.0,
                    19.0,
                    21.0
                ]
                },
                {
                "dimensions": [
                    "HOST-0956C3557E9109C1"
                ],
                "dimensionMap": {
                    "dt.entity.host": "HOST-0956C3557E9109C1"
                },
                "timestamps": [
                    1589456100000,
                    1589456160000,
                    1589456220000
                ],
                "values": [
                    19.0,
                    21.0,
                    22.0
                ]
                }
            ]
            }
        ]
    }
    ```
10. GET AWS supported services
    - Example cURL:
   ```
    https://{{domain}}/api/config/v1/aws/supportedServices
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "services": [
            {
            "cloudProviderServiceType": "AWS/ApiGateway",
            "name": "APIGateway",
            "entityType": "cloud:aws:api_gateway",
            "displayName": "Amazon API Gateway"
            },
            {
            "cloudProviderServiceType": "AWS/RDS",
            "name": "Aurora",
            "entityType": "cloud:aws:aurora",
            "displayName": "Amazon Aurora"
            },
            {
            "cloudProviderServiceType": "AWS/Neptune",
            "name": "neptune",
            "entityType": "cloud:aws:neptune",
            "displayName": "Amazon Neptune"
            }
        ]
    }
    ```
11. GET all dashboards
    - Example cURL:
   ```
    https://{{domain}}/api/config/v1/dashboards
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "dashboards": [
            {
                "id": "22471a3e-4bb3-11ed-bdc3-0242ac120002",
                "name": "OneAgent Traces - Adaptive traffic management (Classic License)",
                "owner": "Dynatrace"
            },
            {
                "id": "3b9c20e2-dc58-4a91-8dcb-f6217dc869ac",
                "name": "Metric & Dimension Usage + Rejections",
                "owner": "Dynatrace"
            },
            {
                "id": "6b38732e-d26b-45c7-b107-ed85e87ff288",
                "name": "Kubernetes workload overview",
                "owner": "Dynatrace"
            },
            {
                "id": "c704bd72-92e9-452a-b40e-73e6f4df9f08",
                "name": "Real User Monitoring",
                "owner": "Dynatrace"
            },
            {
                "id": "b6fc0160-9332-454f-a7bc-7217b2ae540c",
                "name": "Synthetic Monitoring",
                "owner": "Dynatrace"
            },
            {
                "id": "c15f39a8-7d74-4b97-af28-0b17a20dc711",
                "name": "Davis® health self-monitoring",
                "owner": "Dynatrace"
            },
            {
                "id": "6b38732e-8c5c-4b32-80a1-7053ec8f37e1",
                "name": "Kubernetes cluster overview",
                "owner": "Dynatrace"
            },
            {
                "id": "6b38732e-609c-44e2-b34d-0286717ecdab",
                "name": "Kubernetes namespace resource quotas",
                "owner": "Dynatrace"
            }
        ]
    }
    ```
12. GET all users
    - Example cURL:
   ```
    https://{{domain}}/iam/v1/accounts/{accountUuid}/users
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "count": 2,
        "items": [
            {
            "uid": "44fc26d0-ed1f-4fbd-96e8-5da7c192f9c1",
            "email": "john.smith@company.com",
            "name": "John",
            "surname": "Smith",
            "emergencyContact": true,
            "userStatus": "ACTIVE",
            "userLoginMetadata": {
                "successfulLoginCounter": 1260,
                "failedLoginCounter": 0,
                "lastSuccessfulLogin": "2020-03-11T03:01:00Z",
                "lastFailedLogin": null,
                "resetPasswordTokenSentAt": null,
                "lastSuccessfulBasicAuthentication": null,
                "createdAt": "2020-03-11T03:01:00Z",
                "updatedAt": "2020-03-11T03:01:00Z"
            }
            },
            {
            "uid": "20cc1c46-870e-48ca-ac40-9a8459cf6632",
            "email": "jane.brown@company.com",
            "name": "Jane",
            "surname": "Brown",
            "emergencyContact": false,
            "userStatus": "ACTIVE",
            "userLoginMetadata": {
                "successfulLoginCounter": 808,
                "failedLoginCounter": 0,
                "lastSuccessfulLogin": "2020-03-11T03:01:00Z",
                "lastFailedLogin": null,
                "resetPasswordTokenSentAt": null,
                "lastSuccessfulBasicAuthentication": null,
                "createdAt": "2020-03-11T03:01:00Z",
                "updatedAt": "2020-03-11T03:01:00Z"
            }
            }
        ]
    }
    ```
13. GET all groups
    - Example cURL:
    ```
    https://{{domain}}/iam/v1/accounts/{accountUuid}/groups
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "count": 14,
        "items": [
            {
            "uuid": "7a1d224d-0ebc-4318-ab1e-64b217b7c156",
            "name": "Monitoring viewer",
            "owner": "LOCAL",
            "description": null,
            "hidden": false,
            "createdAt": "2020-03-11T03:01:00Z",
            "updatedAt": "2020-03-11T03:01:00Z"
            },
                {
            "uuid": "f335c6ae-f046-48ad-a0a2-49bb8fdca07b",
            "name": "Monitoring admin",
            "owner": "LOCAL",
            "description": null,
            "hidden": false,
            "createdAt": "2020-03-11T03:01:00Z",
            "updatedAt": "2020-03-11T03:01:00Z"
            },
            {
            "uuid": "56d56aba-c12f-44c1-a0ba-42eba3e3ff84",
            "name": "Account manager",
            "owner": "LOCAL",
            "description": null,
            "hidden": false,
            "createdAt": "2020-03-11T03:01:00Z",
            "updatedAt": "2020-03-11T03:01:00Z"
            }
        ]
    }
    ```
14. GET permissions
    - Example cURL:
    ```
    https://{{domain}}/iam/v1/accounts/{accountUuid}/groups/{groupUuid}/permissions
    --request GET \
    --header "Accept:application/json" "Authorization: Api-Token {{a unique token}}"
   ```
   - Response
    ```
    {
        "uuid": "752d4f22-83f9-44dd-8fb2-7f226354fdb5",
        "name": "Finance admin",
        "owner": "LOCAL",
        "description": null,
        "hidden": false,
        "createdAt": "2020-03-11T03:01:00Z",
        "updatedAt": "2020-03-11T03:01:00Z",
        "permissions": [
            {
            "permissionName": "account-viewer",
            "scope": "9ad20784-76c6-4167-bfba-9b0d8d72a71d",
            "scopeType": "account",
            "createdAt": "2020-03-11T03:01:00Z",
            "updatedAt": "2020-03-11T03:01:00Z"
            },
            {
            "permissionName": "account-company-info",
            "scope": "9ad20784-76c6-4167-bfba-9b0d8d72a71d",
            "scopeType": "account",
            "createdAt": "2020-03-11T03:01:00Z",
            "updatedAt": "2020-03-11T03:01:00Z"
            }
        ]
    }
    ```
