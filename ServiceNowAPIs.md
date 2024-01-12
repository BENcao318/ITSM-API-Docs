### ServiceNow API
1. Get Incident Table
   - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/table/incident?sysparm_limit=1
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
    "result": [
        {
            "parent": "",
            "made_sla": "true",
            "caused_by": "",
            "watch_list": "",
            "upon_reject": "cancel",
            "sys_updated_on": "2016-12-14 02:46:44",
            "child_incidents": "0",
            "hold_reason": "",
            "origin_table": "",
            "task_effective_number": "INC0000060",
            "approval_history": "",
            "number": "INC0000060",
            "resolved_by": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user/5137153cc611227c000bbd1bd8cd2007",
                "value": "5137153cc611227c000bbd1bd8cd2007"
            },
            "sys_updated_by": "employee",
            "opened_by": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user/681ccaf9c0a8016400b98a06818d57c7",
                "value": "681ccaf9c0a8016400b98a06818d57c7"
            },
            "user_input": "",
            "sys_created_on": "2016-12-12 15:19:57",
            "sys_domain": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user_group/global",
                "value": "global"
            },
            "state": "7",
            "route_reason": "",
            "sys_created_by": "employee",
            "knowledge": "false",
            "order": "",
            "calendar_stc": "102197",
            "closed_at": "2016-12-14 02:46:44",
            "cmdb_ci": {
                "link": "https://dev226415.service-now.com/api/now/table/cmdb_ci/109562a3c611227500a7b7ff98cc0dc7",
                "value": "109562a3c611227500a7b7ff98cc0dc7"
            },
            "contract": "",
            "impact": "2",
            "active": "false",
            "work_notes_list": "",
            "business_service": {
                "link": "https://dev226415.service-now.com/api/now/table/cmdb_ci_service/27d32778c0a8000b00db970eeaa60f16",
                "value": "27d32778c0a8000b00db970eeaa60f16"
            },
            "business_impact": "",
            "priority": "3",
            "sys_domain_path": "/",
            "rfc": "",
            "time_worked": "",
            "expected_start": "",
            "opened_at": "2016-12-12 15:19:57",
            "business_duration": "1970-01-01 08:00:00",
            "group_list": "",
            "work_end": "",
            "caller_id": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user/681ccaf9c0a8016400b98a06818d57c7",
                "value": "681ccaf9c0a8016400b98a06818d57c7"
            },
            "reopened_time": "",
            "resolved_at": "2016-12-13 21:43:14",
            "approval_set": "",
            "subcategory": "email",
            "work_notes": "",
            "universal_request": "",
            "short_description": "Unable to connect to email",
            "close_code": "Solved (Permanently)",
            "correlation_display": "",
            "work_start": "",
            "assignment_group": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user_group/287ebd7da9fe198100f92cc8d1d2154e",
                "value": "287ebd7da9fe198100f92cc8d1d2154e"
            },
            "additional_assignee_list": "",
            "business_stc": "28800",
            "cause": "",
            "description": "I am unable to connect to the email server. It appears to be down.",
            "origin_id": "",
            "calendar_duration": "1970-01-02 04:23:17",
            "close_notes": "This incident is resolved.",
            "notify": "1",
            "service_offering": "",
            "sys_class_name": "incident",
            "closed_by": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user/681ccaf9c0a8016400b98a06818d57c7",
                "value": "681ccaf9c0a8016400b98a06818d57c7"
            },
            "follow_up": "",
            "parent_incident": "",
            "sys_id": "1c741bd70b2322007518478d83673af3",
            "contact_type": "self-service",
            "reopened_by": "",
            "incident_state": "7",
            "urgency": "2",
            "problem_id": "",
            "company": {
                "link": "https://dev226415.service-now.com/api/now/table/core_company/31bea3d53790200044e0bfc8bcbe5dec",
                "value": "31bea3d53790200044e0bfc8bcbe5dec"
            },
            "reassignment_count": "2",
            "activity_due": "2016-12-13 01:26:36",
            "assigned_to": {
                "link": "https://dev226415.service-now.com/api/now/table/sys_user/5137153cc611227c000bbd1bd8cd2007",
                "value": "5137153cc611227c000bbd1bd8cd2007"
            },
            "severity": "3",
            "comments": "",
            "approval": "not requested",
            "sla_due": "",
            "comments_and_work_notes": "",
            "due_date": "",
            "sys_mod_count": "15",
            "reopen_count": "0",
            "sys_tags": "",
            "escalation": "0",
            "upon_approval": "proceed",
            "correlation_id": "",
            "location": "",
            "category": "inquiry"
            }
        ]
    }
    ```

2. Get Company Table
   - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/table/core_company?sysparm_limit=1
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
    "result": [
        {
            "banner_image_light": "",
            "country": "",
            "parent": "",
            "notes": "",
            "city": "Los Angeles, CA 90028",
            "stock_symbol": "EMC",
            "latitude": "",
            "discount": "",
            "sys_updated_on": "2013-05-06 23:44:48",
            "sys_class_name": "core_company",
            "manufacturer": "true",
            "apple_icon": "",
            "sys_id": "0c43af40c6112275011a4bd4c0143fbf",
            "market_cap": "48930000000",
            "sys_updated_by": "admin",
            "num_employees": "12",
            "fiscal_year": "",
            "rank_tier": "",
            "street": "6922 Hollywood Blvd., 4th floor",
            "sys_created_on": "2005-05-24 01:14:19",
            "vendor": "false",
            "contact": "",
            "lat_long_error": "2: couldn't find this address! sorry",
            "stock_price": "23.29",
            "banner_image": "",
            "state": "",
            "sys_created_by": "guest",
            "longitude": "",
            "vendor_type": "",
            "zip": "",
            "profits": "0",
            "revenue_per_year": "22010000000",
            "website": "www.eatsleepmusic.com",
            "publicly_traded": "false",
            "sys_mod_count": "50",
            "sys_tags": "",
            "fax_phone": "",
            "phone": "1 (800) 958-2983",
            "vendor_manager": "",
            "banner_text": "",
            "name": "N/A",
            "coordinates_retrieved_on": "",
            "customer": "false",
            "primary": "false"
            }
        ]
    }
    ```
3. Get Incident Reporting List
   - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/reporting
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
    "result": {
        "aclRestrictedCount": 8,
        "hasNextPage": true,
        "report": [
            {
                "url": "/report_viewer.do?jvar_report_id=024825220a0a0b5300e711a1a595d384",
                "id": "024825220a0a0b5300e711a1a595d384",
                "title": " KPI - Average Work Effort for Resolving Incidents by Category",
                "type": "pivot",
                "typeDisplayValue": "Pivot Table",
                "table": "incident_time_worked",
                "tableDisplayValue": "Incident Time Worked",
                "updatedOn": "2011-11-30 14:35:43",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=82240486dfb0010068c37a0d3df263b5",
                "id": "82240486dfb0010068c37a0d3df263b5",
                "title": "30/60/90 Day Desired State Task Aging",
                "type": "horizontal_bar",
                "typeDisplayValue": "Horizontal bar",
                "table": "cert_follow_on_task",
                "tableDisplayValue": "Follow On Task",
                "updatedOn": "2013-04-18 13:57:43",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=586cb775dfb0010068c37a0d3df263b8",
                "id": "586cb775dfb0010068c37a0d3df263b8",
                "title": "30/60/90 Day Task Aging",
                "type": "horizontal_bar",
                "typeDisplayValue": "Horizontal bar",
                "table": "cert_follow_on_task",
                "tableDisplayValue": "Follow On Task",
                "updatedOn": "2013-04-18 13:30:43",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=4d6c77790a0a0b300032dd58ee155838",
                "id": "4d6c77790a0a0b300032dd58ee155838",
                "title": "Achieved SLAs by Type",
                "type": "bar",
                "typeDisplayValue": "Bar",
                "table": "task_sla",
                "tableDisplayValue": "Task SLA",
                "updatedOn": "2012-11-29 05:42:30",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=a1849841c611227b01646de563508c09",
                "id": "a1849841c611227b01646de563508c09",
                "title": "Active Change Requests",
                "type": "list",
                "typeDisplayValue": "List",
                "table": "change_request",
                "tableDisplayValue": "Change Request",
                "query": "",
                "updatedOn": "2005-06-21 18:17:56",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=93f4173c53a930104c90ddeeff7b12fa",
                "id": "93f4173c53a930104c90ddeeff7b12fa",
                "title": "Active Incidents older than 7 days",
                "type": "single_score",
                "typeDisplayValue": "Single Score",
                "table": "incident",
                "tableDisplayValue": "Incident",
                "updatedOn": "2021-07-26 15:51:50",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=e9a6c7e6c611227401ddeda261aa53a5",
                "id": "e9a6c7e6c611227401ddeda261aa53a5",
                "title": "Active Releases",
                "type": "list",
                "typeDisplayValue": "List",
                "table": "release_project",
                "tableDisplayValue": "Release",
                "query": "active=true",
                "updatedOn": "2005-08-24 11:01:25",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=e9bcb3f5c611227400be846487861438",
                "id": "e9bcb3f5c611227400be846487861438",
                "title": "Active Releases by Status",
                "type": "list",
                "typeDisplayValue": "List",
                "table": "release_project",
                "tableDisplayValue": "Release",
                "query": "active=true",
                "updatedOn": "2005-08-24 11:25:22",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=3400cdf35f312100a9ad2572f2b47708",
                "id": "3400cdf35f312100a9ad2572f2b47708",
                "title": "Active Requests by Assignee",
                "type": "bar",
                "typeDisplayValue": "Bar",
                "table": "service_task",
                "tableDisplayValue": "Service Task",
                "updatedOn": "2014-07-15 14:13:42",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=c2008df35f312100a9ad2572f2b477a5",
                "id": "c2008df35f312100a9ad2572f2b477a5",
                "title": "Active Requests by Priority",
                "type": "pie",
                "typeDisplayValue": "Pie",
                "table": "service_task",
                "tableDisplayValue": "Service Task",
                "updatedOn": "2014-07-15 14:13:48",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=9300cdf35f312100a9ad2572f2b47727",
                "id": "9300cdf35f312100a9ad2572f2b47727",
                "title": "Active Requests by Service",
                "type": "pie",
                "typeDisplayValue": "Pie",
                "table": "service_task",
                "tableDisplayValue": "Service Task",
                "updatedOn": "2014-07-15 14:13:53",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            },
            {
                "url": "/report_viewer.do?jvar_report_id=b34d4391ff3130106c1ef9a7cddcbdf4",
                "id": "b34d4391ff3130106c1ef9a7cddcbdf4",
                "title": "Active Requests Due Within 5 Days",
                "type": "line_bar",
                "typeDisplayValue": "Column",
                "table": "sc_request",
                "tableDisplayValue": "Request",
                "updatedOn": "2022-04-21 12:02:44",
                "editable": true,
                "published": false,
                "valid": true,
                "favorite": false
            }
        ],
        "hasPreviousPage": false,
        "totalCount": 575
        }
    }
    ```
4. Internal AI Search 
    - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/reporting
    --request POST \
    --header "Accept:application/json" \
    --user 'username':'password'
    --body raw:
    {"rpSysId":"3f1dd0320a0a0b99000a53f7604a2ef9","searchContextConfigId":"2056f9de67621010b3d782f45685efd0","searchTerm":"test"}
   ```
   - Response
    ```
    {
    "result": {
        "search": {
            "term": "test",
            "count": 0,
            "searchResults": []
        },
        "resultsActionsMap": {},
        "availableActions": {
            "40fdb34467fa1010b3d782f45685efe0": {
                "sysId": "40fdb34467fa1010b3d782f45685efe0",
                "actionId": "aisa_resolves",
                "actionLabel": "Solves my issue",
                "restPath": "/resolves",
                "resultTable": null,
                "isCardAction": false,
                "isDetailAction": true,
                "searchApp": null,
                "scriptedVisibility": false,
                "visibilityScript": null,
                "resultTableCondition": null
            },
            "c6eefb4467fa1010b3d782f45685ef55": {
                "sysId": "c6eefb4467fa1010b3d782f45685ef55",
                "actionId": "aisa_sc_cat_item_order",
                "actionLabel": "Order",
                "restPath": "/sc_cat_item_order",
                "resultTable": "sc_cat_item",
                "isCardAction": true,
                "isDetailAction": true,
                "searchApp": null,
                "scriptedVisibility": false,
                "visibilityScript": null,
                "resultTableCondition": "sys_class_name!=sc_cat_item_content^sys_class_name!=sc_cat_item_wizard^EQ"
                }
            }
        }
    }
    ```
5. Retrieve Metadata for attachements
    - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/attachment
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
    "result": [
        {
        "size_bytes": "106879",
        "file_name": "4.3_2_modify-label-names.png",
        "sys_mod_count": "2",
        "average_image_color": "#ffffff",
        "image_width": "800",
        "sys_updated_on": "2016-02-29 16:07:02",
        "sys_tags": "",
        "table_name": "sys_product_help",
        "sys_id": "003a3ef24ff1120031577d2ca310c74b",
        "image_height": "484",
        "sys_updated_by": "admin",
        "download_link": "https://dev226415.service-now.com/api/now/attachment/003a3ef24ff1120031577d2ca310c74b/file",
        "content_type": "image/png",
        "sys_created_on": "2016-02-29 16:07:02",
        "size_compressed": "105563",
        "compressed": "true",
        "state": "",
        "table_sys_id": "750129c94f12020031577d2ca310c7a4",
        "chunk_size_bytes": "",
        "hash": "",
        "sys_created_by": "admin"
        }
    ]
    }
    ```
6. Retrieve attachment metadata
    - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/attachment/{sys_id}
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
7. Get all facets knowledge
   - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/knowledge/search/facets
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
8. Get Advanced chat settings
   - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/advance_chat_settings/get_feature_status
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
    "result": {
        "isMessagePreviewEnabled": false,
        "isProactiveChatEnabled": false
        }
    }
    ```
9.  Get All Data Classes
    - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/data_classification/getAllDataClasses
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
    "result": [
        {
        "parent": {
            "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
            "name": "Confidential"
        },
        "sys_id": "348107b951d71010f877f3f178e7dd0d",
        "name": "Personally identifiable information"
        },
        {
        "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
        "name": "Confidential"
        },
        {
        "sys_id": "59b7070b73fc1010ae8dd21efaf6a764",
        "name": "Restricted"
        },
        {
        "sys_id": "11d60fc773fc1010ae8dd21efaf6a744",
        "name": "Internal"
        },
        {
        "sys_id": "f5b4cf4773fc1010ae8dd21efaf6a766",
        "name": "Public"
        }
            ]
    }
    ```
10. Application Service Internal API
      * Get properties for CI in current/historical map view
    - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/it_service/ciFullData
    --request GET \
    --header "Accept:application/json" \
    --user 'username':'password'
   ```
   - Response
    ```
    {
        "serverData": {
            "changedAttributes": {},
            "metaData": {},
            "relatedItems": [],
            "scalarAttrs": {},
            "tableAttrs": {}
        },
        "vmData": {
            "changedAttributes": {},
            "metaData": {},
            "relatedItems": [],
            "scalarAttrs": {},
            "tableAttrs": {}
        },
        "applicationData": {
            "changedAttributes": {},
            "metaData": {},
            "relatedItems": [],
            "scalarAttrs": {},
            "tableAttrs": {}
        },
        "host": false,
        "endpoint": false,
        "hypervisorData": {
            "changedAttributes": {},
            "metaData": {},
            "relatedItems": [],
            "scalarAttrs": {},
            "tableAttrs": {}
        }
    }
    ```
   
   
   


