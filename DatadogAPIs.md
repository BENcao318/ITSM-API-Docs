### ServiceNow Api
1. Get a list of Audit Logs events
   - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/audit/events
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
    "data": [
        {
        "attributes": {
            "attributes": {
            "customAttribute": 123,
            "duration": 2345
            },
            "message": "string",
            "service": "web-app",
            "tags": [
            "team:A"
            ],
            "timestamp": "2019-01-02T09:42:36.320Z"
        },
        "id": "AAAAAWgN8Xwgr1vKDQAAAABBV2dOOFh3ZzZobm1mWXJFYTR0OA",
        "type": "audit"
        }
    ],
    "links": {
        "next": "https://app.datadoghq.com/api/v2/audit/event?filter[query]=foo\u0026page[cursor]=eyJzdGFydEF0IjoiQVFBQUFYS2tMS3pPbm40NGV3QUFBQUJCV0V0clRFdDZVbG8zY3pCRmNsbHJiVmxDWlEifQ=="
    },
    "meta": {
        "elapsed": 132,
        "page": {
        "after": "eyJzdGFydEF0IjoiQVFBQUFYS2tMS3pPbm40NGV3QUFBQUJCV0V0clRFdDZVbG8zY3pCRmNsbHJiVmxDWlEifQ=="
        },
        "request_id": "MWlFUjVaWGZTTTZPYzM0VXp1OXU2d3xLSVpEMjZKQ0VKUTI0dEYtM3RSOFVR",
        "status": "done",
        "warnings": [
            {
                "code": "unknown_index",
                "detail": "indexes: foo, bar",
                "title": "One or several indexes are missing or invalid, results hold data from the other indexes"
            }
            ]
        }
    }
    ```

2. AWS Integrations: List all AWS integrations
   - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/integration/aws
    --request POST \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
    "accounts": [
            {
            "access_key_id": "string",
            "account_id": "123456789012",
            "account_specific_namespace_rules": {
                "<any-key>": false
            },
            "cspm_resource_collection_enabled": true,
            "excluded_regions": [
                "us-east-1",
                "us-west-2"
            ],
            "filter_tags": [
                "$KEY:$VALUE"
            ],
            "host_tags": [
                "$KEY:$VALUE"
            ],
            "metrics_collection_enabled": false,
            "resource_collection_enabled": true,
            "role_name": "DatadogAWSIntegrationRole",
            "secret_access_key": "string"
            }
        ]
    }
    ```
3. AWS Logs Integration: List all AWS Logs integrations
   - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/integration/aws/logs
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "account_id": "1234567",
        "lambdas": [
            {
            "arn": "arn:aws:lambda:us-east-1:1234567:function:LogsCollectionAPITest"
            }
        ],
        "services": [
            "s3",
            "elb",
            "elbv2",
            "cloudfront",
            "redshift",
            "lambda"
        ]
    }
    ```
4. Azure Integration: List all Azure integrations
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/integration/azure
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "app_service_plan_filters": "key:value,filter:example",
        "automute": true,
        "client_id": "testc7f6-1234-5678-9101-3fcbf464test",
        "client_secret": "testingx./Sw*g/Y33t..R1cH+hScMDt",
        "container_app_filters": "key:value,filter:example",
        "cspm_enabled": true,
        "custom_metrics_enabled": true,
        "errors": [
            "*"
        ],
        "host_filters": "key:value,filter:example",
        "new_client_id": "new1c7f6-1234-5678-9101-3fcbf464test",
        "new_tenant_name": "new1c44-1234-5678-9101-cc00736ftest",
        "resource_collection_enabled": true,
        "tenant_name": "testc44-1234-5678-9101-cc00736ftest"
    }
    ```
5. Get all dashboard lists
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/dashboard/lists/manual
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "dashboard_lists": [
            {
            "author": {
                "email": "string",
                "handle": "string",
                "name": "string"
            },
            "created": "2019-09-19T10:00:00.000Z",
            "dashboard_count": "integer",
            "id": "integer",
            "is_favorite": false,
            "modified": "2019-09-19T10:00:00.000Z",
            "name": "My Dashboard",
            "type": "manual_dashboard_list"
            }
        ]
    }
    ```
6. Get all dashboards
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/dashboard
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
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
7. Get a list of events
   - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/events
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
  ```
    {
        "data": [
            {
            "attributes": {
                "attributes": {
                "aggregation_key": "string",
                "date_happened": "integer",
                "device_name": "string",
                "duration": "integer",
                "event_object": "Did you hear the news today?",
                "evt": {
                    "id": "6509751066204996294",
                    "name": "string",
                    "source_id": 36,
                    "type": "error_tracking_alert"
                },
                "hostname": "string",
                "monitor": {
                    "created_at": 1646318692000,
                    "group_status": "integer",
                    "groups": [],
                    "id": "integer",
                    "message": "string",
                    "modified": "integer",
                    "name": "string",
                    "query": "string",
                    "tags": [
                    "environment:test"
                    ],
                    "templated_name": "string",
                    "type": "string"
                },
                "monitor_groups": [],
                "monitor_id": "integer",
                "priority": "normal",
                "related_event_id": "integer",
                "service": "datadog-api",
                "source_type_name": "string",
                "sourcecategory": "string",
                "status": "info",
                "tags": [
                    "environment:test"
                ],
                "timestamp": 1652274265000,
                "title": "Oh boy!"
                },
                "message": "string",
                "tags": [
                "team:A"
                ],
                "timestamp": "2019-01-02T09:42:36.320Z"
            },
            "id": "AAAAAWgN8Xwgr1vKDQAAAABBV2dOOFh3ZzZobm1mWXJFYTR0OA",
            "type": "event"
            }
        ],
        "links": {
            "next": "https://app.datadoghq.com/api/v2/events?filter[query]=foo\u0026page[cursor]=eyJzdGFydEF0IjoiQVFBQUFYS2tMS3pPbm40NGV3QUFBQUJCV0V0clRFdDZVbG8zY3pCRmNsbHJiVmxDWlEifQ=="
        },
        "meta": {
            "elapsed": 132,
            "page": {
            "after": "eyJzdGFydEF0IjoiQVFBQUFYS2tMS3pPbm40NGV3QUFBQUJCV0V0clRFdDZVbG8zY3pCRmNsbHJiVmxDWlEifQ=="
            },
            "request_id": "MWlFUjVaWGZTTTZPYzM0VXp1OXU2d3xLSVpEMjZKQ0VKUTI0dEYtM3RSOFVR",
            "status": "done",
            "warnings": [
            {
                "code": "unknown_index",
                "detail": "indexes: foo, bar",
                "title": "One or several indexes are missing or invalid. Results hold data from the other indexes."
            }
            ]
        }
    }
  ```
8. Get details of an incident service
   - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/services/{service_id}
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response 
    ```
    {
        "data": {
            "attributes": {
            "created": "2019-09-19T10:00:00.000Z",
            "modified": "2019-09-19T10:00:00.000Z",
            "name": "service name"
            },
            "id": "00000000-0000-0000-0000-000000000000",
            "relationships": {
            "created_by": {
                "data": {
                "id": "00000000-0000-0000-2345-000000000000",
                "type": "users"
                }
            },
            "last_modified_by": {
                "data": {
                "id": "00000000-0000-0000-2345-000000000000",
                "type": "users"
                }
            }
            },
            "type": "services"
        },
        "included": [
            {
            "attributes": {
                "created_at": "2019-09-19T10:00:00.000Z",
                "disabled": false,
                "email": "string",
                "handle": "string",
                "icon": "string",
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "string",
                "service_account": false,
                "status": "string",
                "title": "string",
                "verified": false
            },
            "id": "string",
            "relationships": {
                "org": {
                "data": {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                }
                },
                "other_orgs": {
                "data": [
                    {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                    }
                ]
                },
                "other_users": {
                "data": [
                    {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "users"
                    }
                ]
                },
                "roles": {
                "data": [
                    {
                    "id": "3653d3c6-0c75-11ea-ad28-fb5701eabc7d",
                    "type": "roles"
                    }
                ]
                }
            },
            "type": "users"
            }
        ]
    }
    ```
9.  Get the details of an incident
    - Example cURL:
   ```
    ttps://api.datadoghq.com/api/v2/incidents/{incident_id}
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": {
            "attributes": {
            "archived": "2019-09-19T10:00:00.000Z",
            "case_id": "integer",
            "created": "2019-09-19T10:00:00.000Z",
            "customer_impact_duration": "integer",
            "customer_impact_end": "2019-09-19T10:00:00.000Z",
            "customer_impact_scope": "An example customer impact scope",
            "customer_impact_start": "2019-09-19T10:00:00.000Z",
            "customer_impacted": false,
            "detected": "2019-09-19T10:00:00.000Z",
            "fields": {
                "<any-key>": "undefined"
            },
            "modified": "2019-09-19T10:00:00.000Z",
            "non_datadog_creator": {
                "image_48_px": "string",
                "name": "string"
            },
            "notification_handles": [
                {
                "display_name": "Jane Doe",
                "handle": "@test.user@test.com"
                }
            ],
            "public_id": 1,
            "resolved": "2019-09-19T10:00:00.000Z",
            "severity": "UNKNOWN",
            "state": "string",
            "time_to_detect": "integer",
            "time_to_internal_response": "integer",
            "time_to_repair": "integer",
            "time_to_resolve": "integer",
            "title": "A test incident title",
            "visibility": "string"
            },
            "id": "00000000-0000-0000-1234-000000000000",
            "relationships": {
            "attachments": {
                "data": [
                {
                    "id": "00000000-0000-abcd-1000-000000000000",
                    "type": "incident_attachments"
                }
                ]
            },
            "commander_user": {
                "data": {
                "id": "00000000-0000-0000-0000-000000000000",
                "type": "users"
                }
            },
            "created_by_user": {
                "data": {
                "id": "00000000-0000-0000-2345-000000000000",
                "type": "users"
                }
            },
            "impacts": {
                "data": [
                {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "incident_impacts"
                }
                ]
            },
            "integrations": {
                "data": [
                {
                    "id": "00000000-abcd-0001-0000-000000000000",
                    "type": "incident_integrations"
                }
                ]
            },
            "last_modified_by_user": {
                "data": {
                "id": "00000000-0000-0000-2345-000000000000",
                "type": "users"
                }
            },
            "responders": {
                "data": [
                {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "incident_responders"
                }
                ]
            },
            "user_defined_fields": {
                "data": [
                {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "user_defined_field"
                }
                ]
            }
            },
            "type": "incidents"
        },
        "included": [
            {
            "attributes": {
                "created_at": "2019-09-19T10:00:00.000Z",
                "disabled": false,
                "email": "string",
                "handle": "string",
                "icon": "string",
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "string",
                "service_account": false,
                "status": "string",
                "title": "string",
                "verified": false
            },
            "id": "string",
            "relationships": {
                "org": {
                "data": {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                }
                },
                "other_orgs": {
                "data": [
                    {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                    }
                ]
                },
                "other_users": {
                "data": [
                    {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "users"
                    }
                ]
                },
                "roles": {
                "data": [
                    {
                    "id": "3653d3c6-0c75-11ea-ad28-fb5701eabc7d",
                    "type": "roles"
                    }
                ]
                }
            },
            "type": "users"
            }
        ]
    }
    ```
10. Get IP Allowlist
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/ip_allowlist
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": {
            "attributes": {
            "enabled": false,
            "entries": [
                {
                "data": {
                    "attributes": {
                    "cidr_block": "string",
                    "created_at": "2019-09-19T10:00:00.000Z",
                    "modified_at": "2019-09-19T10:00:00.000Z",
                    "note": "string"
                    },
                    "id": "string",
                    "type": "ip_allowlist_entry"
                }
                }
            ]
            },
            "id": "string",
            "type": "ip_allowlist"
        }
    }
    ```
11. Get all monitor details
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v1/monitor
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "created": "2019-09-19T10:00:00.000Z",
        "creator": {
            "email": "string",
            "handle": "string",
            "name": "string"
        },
        "deleted": "2019-09-19T10:00:00.000Z",
        "id": "integer",
        "matching_downtimes": [
            {
            "end": 1412792983,
            "id": 1625,
            "scope": [
                "env:staging"
            ],
            "start": 1412792983
            }
        ],
        "message": "string",
        "modified": "2019-09-19T10:00:00.000Z",
        "multi": false,
        "name": "My monitor",
        "options": {
            "aggregation": {
            "group_by": "host",
            "metric": "metrics.name",
            "type": "count"
            },
            "device_ids": [],
            "enable_logs_sample": false,
            "enable_samples": false,
            "escalation_message": "string",
            "evaluation_delay": "integer",
            "group_retention_duration": "string",
            "groupby_simple_monitor": false,
            "include_tags": false,
            "locked": false,
            "min_failure_duration": "integer",
            "min_location_failed": "integer",
            "new_group_delay": "integer",
            "new_host_delay": "integer",
            "no_data_timeframe": "integer",
            "notification_preset_name": "string",
            "notify_audit": false,
            "notify_by": [],
            "notify_no_data": false,
            "on_missing_data": "string",
            "renotify_interval": "integer",
            "renotify_occurrences": "integer",
            "renotify_statuses": [],
            "require_full_window": false,
            "scheduling_options": {
            "custom_schedule": {
                "recurrences": [
                {
                    "rrule": "FREQ=WEEKLY;BYDAY=MO,TU,WE,TH,FR",
                    "start": "2023-08-31T16:30:00",
                    "timezone": "Europe/Paris"
                }
                ]
            },
            "evaluation_window": {
                "day_starts": "04:00",
                "hour_starts": 0,
                "month_starts": 1
            }
            },
            "silenced": {
            "<any-key>": "integer"
            },
            "synthetics_check_id": "string",
            "threshold_windows": {
            "recovery_window": "string",
            "trigger_window": "string"
            },
            "thresholds": {
            "critical": "number",
            "critical_recovery": "number",
            "ok": "number",
            "unknown": "number",
            "warning": "number",
            "warning_recovery": "number"
            },
            "timeout_h": "integer",
            "variables": [
            {
                "compute": {
                "aggregation": "avg",
                "interval": 60000,
                "metric": "@duration"
                },
                "data_source": "rum",
                "group_by": [
                {
                    "facet": "status",
                    "limit": 10,
                    "sort": {
                    "aggregation": "avg",
                    "metric": "string",
                    "order": "string"
                    }
                }
                ],
                "indexes": [
                "days-3",
                "days-7"
                ],
                "name": "query_errors",
                "search": {
                "query": "service:query"
                }
            }
            ]
        },
        "overall_state": "string",
        "priority": "integer",
        "query": "avg(last_5m):sum:system.net.bytes_rcvd{host:host0} > 100",
        "restricted_roles": [],
        "state": {
            "groups": {
            "<any-key>": {
                "last_nodata_ts": "integer",
                "last_notified_ts": "integer",
                "last_resolved_ts": "integer",
                "last_triggered_ts": "integer",
                "name": "string",
                "status": "string"
            }
            }
        },
        "tags": [],
        "type": "query alert"
    }
    ```
12. Get a list of permissions
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/permissions
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "created": "2019-09-19T10:00:00.000Z",
                "description": "string",
                "display_name": "string",
                "display_type": "string",
                "group_name": "string",
                "name": "string",
                "restricted": false
            },
            "id": "string",
            "type": "permissions"
            }
        ]
    }
    ```
13. Get a list of roles
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/roles
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "created_at": "2019-09-19T10:00:00.000Z",
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "string",
                "user_count": "integer"
            },
            "id": "string",
            "relationships": {
                "permissions": {
                "data": [
                    {
                    "id": "string",
                    "type": "permissions"
                    }
                ]
                }
            },
            "type": "roles"
            }
        ],
        "meta": {
            "page": {
            "total_count": "integer",
            "total_filtered_count": "integer"
            }
        }
    }
    ```
14. Security Monitoring: List findings
    - Example cURL:
   ```
     https://api.datadoghq.com/api/v2/posture_management/findings
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "evaluation": "pass",
                "evaluation_changed_at": 1678721573794,
                "mute": {
                "description": "To be resolved later",
                "expiration_date": 1778721573794,
                "muted": true,
                "reason": "ACCEPTED_RISK",
                "start_date": 1678721573794,
                "uuid": "e51c9744-d158-11ec-ad23-da7ad0900002"
                },
                "resource": "my_resource_name",
                "resource_discovery_date": 1678721573794,
                "resource_type": "azure_storage_account",
                "rule": {
                "id": "dv2-jzf-41i",
                "name": "Soft delete is enabled for Azure Storage"
                },
                "status": "critical",
                "tags": [
                "cloud_provider:aws",
                "myTag:myValue"
                ]
            },
            "id": "ZGVmLTAwcC1pZXJ-aS0wZjhjNjMyZDNmMzRlZTgzNw==",
            "type": "finding"
            }
        ],
        "meta": {
            "page": {
            "cursor": "eyJhZnRlciI6IkFRQUFBWWJiaEJXQS1OY1dqUUFBQUFCQldXSmlhRUpYUVVGQlJFSktkbTlDTUdaWFRVbDNRVUUiLCJ2YWx1ZXMiOlsiY3JpdGljYWwiXX0=",
            "total_filtered_count": 213
            },
            "snapshot_timestamp": 1678721573794
        }
    }
    ```
15. Security Monitoring: Get a list of security signals
    - Example cURL:
   ```
     https://api.datadoghq.com/api/v2/security_monitoring/signals/search
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "custom": {
                "workflow": {
                    "first_seen": "2020-06-23T14:46:01.000Z",
                    "last_seen": "2020-06-23T14:46:49.000Z",
                    "rule": {
                    "id": "0f5-e0c-805",
                    "name": "Brute Force Attack Grouped By User ",
                    "version": 12
                    }
                }
                },
                "message": "Detect Account Take Over (ATO) through brute force attempts",
                "tags": [
                "security:attack",
                "technique:T1110-brute-force"
                ],
                "timestamp": "2019-01-02T09:42:36.320Z"
            },
            "id": "AAAAAWgN8Xwgr1vKDQAAAABBV2dOOFh3ZzZobm1mWXJFYTR0OA",
            "type": "signal"
            }
        ],
        "links": {
            "next": "https://app.datadoghq.com/api/v2/security_monitoring/signals?filter[query]=foo\u0026page[cursor]=eyJzdGFydEF0IjoiQVFBQUFYS2tMS3pPbm40NGV3QUFBQUJCV0V0clRFdDZVbG8zY3pCRmNsbHJiVmxDWlEifQ=="
        },
        "meta": {
            "page": {
            "after": "eyJzdGFydEF0IjoiQVFBQUFYS2tMS3pPbm40NGV3QUFBQUJCV0V0clRFdDZVbG8zY3pCRmNsbHJiVmxDWlEifQ=="
            }
        }
    }
    ```
16. Sensitive Data Scanner: List Scanning Groups
    - Example cURL:
   ```
      https://api.datadoghq.com/api/v2/sensitive-data-scanner/config
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": {
            "attributes": {},
            "id": "string",
            "relationships": {
            "groups": {
                "data": [
                {
                    "id": "string",
                    "type": "sensitive_data_scanner_group"
                }
                ]
            }
            },
            "type": "sensitive_data_scanner_configuration"
        },
        "included": [
            {
            "attributes": {
                "description": "string",
                "excluded_namespaces": [
                "admin.name"
                ],
                "is_enabled": false,
                "name": "string",
                "namespaces": [
                "admin"
                ],
                "pattern": "string",
                "priority": "integer",
                "tags": [],
                "text_replacement": {
                "number_of_chars": "integer",
                "replacement_string": "string",
                "type": "string"
                }
            },
            "id": "string",
            "relationships": {
                "group": {
                "data": {
                    "id": "string",
                    "type": "sensitive_data_scanner_group"
                }
                },
                "standard_pattern": {
                "data": {
                    "id": "string",
                    "type": "sensitive_data_scanner_standard_pattern"
                }
                }
            },
            "type": "sensitive_data_scanner_rule"
            }
        ],
        "meta": {
            "count_limit": "integer",
            "group_count_limit": "integer",
            "has_highlight_enabled": false,
            "has_multi_pass_enabled": false,
            "is_pci_compliant": false,
            "version": 0
        }
    }
    ```
17. Sensitive Data Scanner: List standard patterns
    - Example cURL:
   ```
      https://api.datadoghq.com/api/v2/sensitive-data-scanner/config/standard-patterns
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "description": "string",
                "included_keywords": [],
                "name": "string",
                "pattern": "string",
                "priority": "integer",
                "tags": []
            },
            "id": "string",
            "type": "sensitive_data_scanner_standard_pattern"
            }
        ]
    }
    ```
18. Service Definition: Get all service definitions
    - Example cURL:
   ```
      https://api.datadoghq.com/api/v2/services/definitions
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "meta": {
                "github-html-url": "string",
                "ingested-schema-version": "string",
                "ingestion-source": "string",
                "last-modified-time": "string",
                "origin": "string",
                "origin-detail": "string",
                "warnings": [
                    {
                    "instance-location": "string",
                    "keyword-location": "string",
                    "message": "string"
                    }
                ]
                },
                "schema": {
                "contact": {
                    "email": "contact@datadoghq.com",
                    "slack": "https://yourcompany.slack.com/archives/channel123"
                },
                "extensions": {
                    "myorg/extension": "extensionValue"
                },
                "external-resources": [
                    {
                    "name": "Runbook",
                    "type": "runbook",
                    "url": "https://my-runbook"
                    }
                ],
                "info": {
                    "dd-service": "myservice",
                    "description": "A shopping cart service",
                    "display-name": "My Service",
                    "service-tier": "Tier 1"
                },
                "integrations": {
                    "pagerduty": "https://my-org.pagerduty.com/service-directory/PMyService"
                },
                "org": {
                    "application": "E-Commerce",
                    "team": "my-team"
                },
                "schema-version": "v1",
                "tags": [
                    "my:tag",
                    "service:tag"
                ]
                }
            },
            "id": "string",
            "type": "string"
            }
        ]
    }
    ```
19. Service Dependencies: Get all service dependencies
    - Example cURL:
   ```
      https://api.datadoghq.com/api/v1/service_dependencies
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "servica_a": {
            "calls": [
            "service_b",
            "service_c"
            ]
        },
        "service_b": {
            "calls": [
            "service_o"
            ]
        },
        "service_c": {
            "calls": [
            "service_o"
            ]
        },
        "service_o": {
            "calls": []
        }
    }
    ```
20. Get all teams
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/team
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "avatar": "🥑",
                "banner": "integer",
                "created_at": "2019-09-19T10:00:00.000Z",
                "description": "string",
                "handle": "example-team",
                "hidden_modules": [],
                "link_count": "integer",
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "Example Team",
                "summary": "string",
                "user_count": "integer",
                "visible_modules": []
            },
            "id": "aeadc05e-98a8-11ec-ac2c-da7ad0900001",
            "relationships": {
                "team_links": {
                "data": [
                    {
                    "id": "f9bb8444-af7f-11ec-ac2c-da7ad0900001",
                    "type": "team_links"
                    }
                ],
                "links": {
                    "related": "/api/v2/team/c75a4a8e-20c7-11ee-a3a5-da7ad0900002/links"
                }
                },
                "user_team_permissions": {
                "data": {
                    "id": "UserTeamPermissions-aeadc05e-98a8-11ec-ac2c-da7ad0900001-416595",
                    "type": "user_team_permissions"
                },
                "links": {
                    "related": "/api/v2/team/c75a4a8e-20c7-11ee-a3a5-da7ad0900002/links"
                }
                }
            },
            "type": "team"
            }
        ],
        "included": [
            {
            "attributes": {
                "created_at": "2019-09-19T10:00:00.000Z",
                "disabled": false,
                "email": "string",
                "handle": "string",
                "icon": "string",
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "string",
                "service_account": false,
                "status": "string",
                "title": "string",
                "verified": false
            },
            "id": "string",
            "relationships": {
                "org": {
                "data": {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                }
                },
                "other_orgs": {
                "data": [
                    {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                    }
                ]
                },
                "other_users": {
                "data": [
                    {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "users"
                    }
                ]
                },
                "roles": {
                "data": [
                    {
                    "id": "3653d3c6-0c75-11ea-ad28-fb5701eabc7d",
                    "type": "roles"
                    }
                ]
                }
            },
            "type": "users"
            }
        ],
        "links": {
            "first": "string",
            "last": "string",
            "next": "string",
            "prev": "string",
            "self": "string"
        },
        "meta": {
            "pagination": {
            "first_offset": "integer",
            "last_offset": "integer",
            "limit": "integer",
            "next_offset": "integer",
            "offset": "integer",
            "prev_offset": "integer",
            "total": "integer",
            "type": "string"
            }
        }
    }
    ```
21. Usage Metering: Get hourly usage by product family
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/usage/hourly_usage
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "measurements": [
                {
                    "usage_type": "string",
                    "value": "integer"
                }
                ],
                "org_name": "string",
                "product_family": "string",
                "public_id": "string",
                "region": "string",
                "timestamp": "2019-09-19T10:00:00.000Z"
            },
            "id": "string",
            "type": "usage_timeseries"
            }
        ],
        "meta": {
            "pagination": {
            "next_record_id": "string"
            }
        }
    }
    ```
22. List all users
    - Example cURL:
   ```
    https://api.datadoghq.com/api/v2/users
    --request GET \
    --header "Accept:application/json" \
    --DD_SITE="datadoghq.com" DD_API_KEY="<API-KEY>" DD_APP_KEY="<APP-KEY>"
   ```
   - Response
    ```
    {
        "data": [
            {
            "attributes": {
                "created_at": "2019-09-19T10:00:00.000Z",
                "disabled": false,
                "email": "string",
                "handle": "string",
                "icon": "string",
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "string",
                "service_account": false,
                "status": "string",
                "title": "string",
                "verified": false
            },
            "id": "string",
            "relationships": {
                "org": {
                "data": {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                }
                },
                "other_orgs": {
                "data": [
                    {
                    "id": "00000000-0000-beef-0000-000000000000",
                    "type": "orgs"
                    }
                ]
                },
                "other_users": {
                "data": [
                    {
                    "id": "00000000-0000-0000-2345-000000000000",
                    "type": "users"
                    }
                ]
                },
                "roles": {
                "data": [
                    {
                    "id": "3653d3c6-0c75-11ea-ad28-fb5701eabc7d",
                    "type": "roles"
                    }
                ]
                }
            },
            "type": "users"
            }
        ],
        "included": [
            {
            "attributes": {
                "created_at": "2019-09-19T10:00:00.000Z",
                "description": "string",
                "disabled": false,
                "modified_at": "2019-09-19T10:00:00.000Z",
                "name": "string",
                "public_id": "string",
                "sharing": "string",
                "url": "string"
            },
            "id": "string",
            "type": "orgs"
            }
        ],
        "meta": {
            "page": {
            "total_count": "integer",
            "total_filtered_count": "integer"
            }
        }
    }
    ```
    
   
   
   


