### Splunk API
1. Get List of Applications Installed On The Server
   - Example cURL:
   ```
    https://{{sn_instance}}.service-now.com/api/now/table/incident?sysparm_limit=1
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>localapps</title>
        <id>https://localhost:8089/services/apps/local</id>
        <updated>2023-12-19T10:40:26-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/apps/local/_new" rel="create"/>
        <link href="/services/apps/local/_reload" rel="_reload"/>
        <opensearch:totalResults>21</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>alert_logevent</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/alert_logevent</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_logevent/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Log Event Alert Action</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Log Event Alert Action</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">9.1.2</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>alert_webhook</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/alert_webhook</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/alert_webhook/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Webhook Alert Action</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Webhook Alert Action</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">9.1.2</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>appsbrowser</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/appsbrowser</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/appsbrowser" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/appsbrowser" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/appsbrowser/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/appsbrowser" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/appsbrowser/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Browse apps available to install.</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Apps Browser</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">9.1.2</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>introspection_generator_addon</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/introspection_generator_addon</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/introspection_generator_addon/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Affords and supports the Platform Instrumentation initiative.</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">introspection_generator_addon</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">9.1.2</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>launcher</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/launcher</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/launcher" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/launcher" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/launcher/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/launcher" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/launcher/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Home</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="supported_themes">light,dark</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>learned</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/learned</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/learned" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/learned" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/learned/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/learned" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/learned" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/learned/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/learned/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">learned</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>legacy</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/legacy</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/legacy" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/legacy" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/legacy/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/legacy" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/legacy" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/legacy/enable" rel="enable"/>
            <link href="/servicesNS/nobody/system/apps/local/legacy/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">1</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">legacy</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>python_upgrade_readiness_app</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/python_upgrade_readiness_app/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk Inc.</s:key>
                    <s:key name="build">95</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Use this app to prepare your Splunk platform instance for upgrade to the version that includes the Python 3.7 runtime and jQuery 3.5 and above.</s:key>
                    <s:key name="details">https://apps.splunk.com/apps/id/python_upgrade_readiness_app</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>sc_admin</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>sc_admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Upgrade Readiness App</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">4.1.2</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>sample_app</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/sample_app</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/sample_app" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/sample_app" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/sample_app/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/sample_app" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/sample_app" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/sample_app/enable" rel="enable"/>
            <link href="/servicesNS/nobody/system/apps/local/sample_app/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">1</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">sample data</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>search</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/search</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/search" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/search" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/search/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/search" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/search/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">
                        <![CDATA[The Search app is Splunk's default interface for searching and analyzing IT data. It allows you to index data into Splunk, add knowledge, build reports, and create alerts. The Search app can be used across many areas of IT including application management, operations management, security, and compliance.]]>
                    </s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Search &amp; Reporting</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="supported_themes">light,dark</s:key>
                    <s:key name="version">9.1.2</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk-dashboard-studio</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk-dashboard-studio</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk-dashboard-studio/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="build">1296413066</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Splunk dashboard studio</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Splunk Dashboard Studio</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">1.11.7</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_assist</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_assist</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_assist" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_assist" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_assist/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_assist" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_assist/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="build">1</s:key>
                    <s:key name="check_for_updates">0</s:key>
                    <s:key name="configured">1</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Splunk Assist</s:key>
                    <s:key name="details">https://apps.splunk.com/apps/id/assist</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Splunk Assist</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">1.0.3</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_gdi</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_gdi</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_gdi" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_gdi" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_gdi/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_gdi" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_gdi/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="build">0</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Splunk Get Data In</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Splunk Get Data In</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">1.0.6</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_httpinput</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_httpinput</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_httpinput/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">splunk_httpinput</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_instrumentation</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_instrumentation</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_instrumentation" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_instrumentation" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_instrumentation/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_instrumentation" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_instrumentation/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">This application connects the hosting Splunk instance to Splunk's usage data collection services.</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Instrumentation</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">6.0.10</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_internal_metrics</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_internal_metrics</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_internal_metrics/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Clones, converts and stores various internal splunk logs into _metrics index</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Clones Internal Metrics into Metrics Index</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_metrics_workspace</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_metrics_workspace</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_metrics_workspace/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="build">224180260</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Compare trends in time series</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Splunk Analytics Workspace</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="supported_themes">light,dark</s:key>
                    <s:key name="version">2.45.0</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_monitoring_console</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_monitoring_console</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_monitoring_console/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk</s:key>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">The Splunk Monitoring Console application gives you insight into your Splunk deployment.</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Monitoring Console</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">0</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">9.1.2</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>splunk_secure_gateway</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/splunk_secure_gateway</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway/disable" rel="disable"/>
            <link href="/servicesNS/nobody/system/apps/local/splunk_secure_gateway/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="author">Splunk Inc.</s:key>
                    <s:key name="build">55815453</s:key>
                    <s:key name="check_for_updates">0</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="description">Splunk Secure Gateway</s:key>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>sc_admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">Splunk Secure Gateway</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="version">3.4.255</s:key>
                    <s:key name="visible">1</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>SplunkForwarder</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/SplunkForwarder</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder/enable" rel="enable"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkForwarder/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">1</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">SplunkForwarder</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>SplunkLightForwarder</title>
            <id>https://localhost:8089/servicesNS/nobody/system/apps/local/SplunkLightForwarder</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder" rel="list"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder" rel="edit"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder" rel="remove"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder/enable" rel="enable"/>
            <link href="/servicesNS/nobody/system/apps/local/SplunkLightForwarder/package" rel="package"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="check_for_updates">1</s:key>
                    <s:key name="configured">0</s:key>
                    <s:key name="core">1</s:key>
                    <s:key name="disabled">1</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">system</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">app</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="label">SplunkLightForwarder</s:key>
                    <s:key name="managed_by_deployment_client">0</s:key>
                    <s:key name="show_in_nav">1</s:key>
                    <s:key name="state_change_requires_restart">0</s:key>
                    <s:key name="visible">0</s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
    ```

2. Create Messages
   - Example cURL:
   ```
    https://localhost:8089/services/messages
    --request POST \
    --user 'username':'password'
    --body
        name:sampleMessage
        value:"This is a sample message. 2"
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>messages</title>
        <id>https://localhost:8089/services/messages</id>
        <updated>2023-12-19T11:11:04-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/messages/_new" rel="create"/>
        <opensearch:totalResults>1</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>sampleMessage</title>
            <id>https://localhost:8089/services/messages/sampleMessage</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/services/messages/sampleMessage" rel="alternate"/>
            <author>
                <name>system</name>
            </author>
            <link href="/services/messages/sampleMessage" rel="remove"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="capabilities">
                        <s:list/>
                    </s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app"></s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">0</s:key>
                            <s:key name="owner">system</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                            <s:item>splunk-system-role</s:item>
                                            <s:item>user</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">system</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="help"></s:key>
                    <s:key name="message">"This is a sample message. 2"</s:key>
                    <s:key name="message_alternate"></s:key>
                    <s:key name="sampleMessage">"This is a sample message. 2"</s:key>
                    <s:key name="server">1JTWA75562</s:key>
                    <s:key name="severity">warn</s:key>
                    <s:key name="timeCreated_epochSecs">1703002264</s:key>
                    <s:key name="timeCreated_iso">2023-12-19T11:11:04-05:00</s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
    ```
3. Read All Messages
   - Example cURL:
   ```
    https://localhost:8089/services/messages
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>messages</title>
        <id>https://localhost:8089/services/messages</id>
        <updated>2023-12-19T11:11:59-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/messages/_new" rel="create"/>
        <opensearch:totalResults>1</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>sampleMessage</title>
            <id>https://localhost:8089/services/messages/sampleMessage</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/services/messages/sampleMessage" rel="alternate"/>
            <author>
                <name>system</name>
            </author>
            <link href="/services/messages/sampleMessage" rel="remove"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="capabilities">
                        <s:list/>
                    </s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app"></s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">0</s:key>
                            <s:key name="owner">system</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                            <s:item>splunk-system-role</s:item>
                                            <s:item>user</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">system</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="help"></s:key>
                    <s:key name="message">"This is a sample message. 2"</s:key>
                    <s:key name="message_alternate"></s:key>
                    <s:key name="sampleMessage">"This is a sample message. 2"</s:key>
                    <s:key name="server">1JTWA75562</s:key>
                    <s:key name="severity">warn</s:key>
                    <s:key name="timeCreated_epochSecs">1703002264</s:key>
                    <s:key name="timeCreated_iso">2023-12-19T11:11:04-05:00</s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
    ```
4. Access LDAP Configuration Strategies
    - Example cURL:
   ```
    https://localhost:8089/services/authentication/providers/LDAP
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>LDAP-auth</title>
        <id>https://localhost:8089/services/authentication/providers/LDAP</id>
        <updated>2023-12-19T11:13:12-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/authentication/providers/LDAP/_new" rel="create"/>
        <opensearch:totalResults>0</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
    </feed>
    ```
5. Get List Of Installed App Templates
    - Example cURL:
   ```
    https://localhost:8089/services/apps/apptemplates
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title></title>
        <id>https://localhost:8089/services/apps/apptemplates</id>
        <updated>2023-12-19T11:14:18-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <opensearch:totalResults>2</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>barebones</title>
            <id>https://localhost:8089/services/apps/apptemplates/barebones</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/services/apps/apptemplates/barebones" rel="alternate"/>
            <author>
                <name>system</name>
            </author>
            <link href="/services/apps/apptemplates/barebones" rel="list"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app"></s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">0</s:key>
                            <s:key name="owner">system</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>splunk-system-role</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">system</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="lol">wut</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>sample_app</title>
            <id>https://localhost:8089/services/apps/apptemplates/sample_app</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/services/apps/apptemplates/sample_app" rel="alternate"/>
            <author>
                <name>system</name>
            </author>
            <link href="/services/apps/apptemplates/sample_app" rel="list"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app"></s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">0</s:key>
                            <s:key name="owner">system</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>splunk-system-role</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">system</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="lol">wut</s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
    ```
6. Manage cluster node configuration details
    - Example cURL:
   ```
    https://localhost:8089/services/cluster/config/config
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
   ```
   <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>clusterconfig</title>
        <id>https://localhost:8089/services/cluster/config</id>
        <updated>2023-12-19T11:15:30-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/cluster/config/_reload" rel="_reload"/>
        <link href="/services/cluster/config/_acl" rel="_acl"/>
        <opensearch:totalResults>1</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>config</title>
            <id>https://localhost:8089/services/cluster/config/config</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/services/cluster/config/config" rel="alternate"/>
            <author>
                <name>system</name>
            </author>
            <link href="/services/cluster/config/config" rel="list"/>
            <link href="/services/cluster/config/config/_reload" rel="_reload"/>
            <link href="/services/cluster/config/config" rel="edit"/>
            <link href="/services/cluster/config/config/enable" rel="enable"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="access_logging_for_heartbeats">1</s:key>
                    <s:key name="cluster_label"></s:key>
                    <s:key name="cm_com_timeout">18446744073709551615</s:key>
                    <s:key name="cm_heartbeat_period">1</s:key>
                    <s:key name="cm_max_hbmiss_count">3</s:key>
                    <s:key name="cxn_timeout">60</s:key>
                    <s:key name="disabled">1</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app"></s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">0</s:key>
                            <s:key name="owner">system</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>splunk-system-role</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>splunk-system-role</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">system</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:attributes">
                        <s:dict>
                            <s:key name="optionalFields">
                                <s:list>
                                    <s:item>access_logging_for_heartbeats</s:item>
                                    <s:item>ack_factor</s:item>
                                    <s:item>allow_default_empty_p4symmkey</s:item>
                                    <s:item>allowed_hbmiss_count</s:item>
                                    <s:item>assign_primaries_to_all_sites</s:item>
                                    <s:item>auto_rebalance_primaries</s:item>
                                    <s:item>available_sites</s:item>
                                    <s:item>backup_and_restore_primaries_in_maintenance</s:item>
                                    <s:item>buckets_per_addpeer</s:item>
                                    <s:item>buckets_to_summarize</s:item>
                                    <s:item>bucketsize_mismatch_strategy</s:item>
                                    <s:item>bucketsize_upload_preference</s:item>
                                    <s:item>cluster_label</s:item>
                                    <s:item>cm_com_timeout</s:item>
                                    <s:item>cm_heartbeat_period</s:item>
                                    <s:item>cm_max_hbmiss_count</s:item>
                                    <s:item>commit_generation_execution_limit_ms</s:item>
                                    <s:item>cxn_timeout</s:item>
                                    <s:item>decommission_force_finish_idle_time</s:item>
                                    <s:item>decommission_force_timeout</s:item>
                                    <s:item>decommission_node_force_timeout</s:item>
                                    <s:item>decommission_search_jobs_wait_secs</s:item>
                                    <s:item>enable_parallel_add_peer</s:item>
                                    <s:item>enable_primary_fixup_during_maintenance</s:item>
                                    <s:item>executor_workers</s:item>
                                    <s:item>forwarder_site_failover</s:item>
                                    <s:item>freeze_during_maintenance</s:item>
                                    <s:item>generation_poll_interval</s:item>
                                    <s:item>health_report_period</s:item>
                                    <s:item>heartbeat_period</s:item>
                                    <s:item>heartbeat_timeout</s:item>
                                    <s:item>localization_based_primary_selection</s:item>
                                    <s:item>localization_update_batch_size</s:item>
                                    <s:item>manager_switchover_mode</s:item>
                                    <s:item>manager_switchover_quiet_period</s:item>
                                    <s:item>manager_uri</s:item>
                                    <s:item>manual_detention</s:item>
                                    <s:item>master_uri</s:item>
                                    <s:item>max_auto_service_interval</s:item>
                                    <s:item>max_concurrent_peers_joining</s:item>
                                    <s:item>max_fixup_time_ms</s:item>
                                    <s:item>max_nonhot_rep_kBps</s:item>
                                    <s:item>max_peer_batch_rep_load</s:item>
                                    <s:item>max_peer_build_load</s:item>
                                    <s:item>max_peer_rep_load</s:item>
                                    <s:item>max_peer_sum_rep_load</s:item>
                                    <s:item>max_peers_to_download_bundle</s:item>
                                    <s:item>max_primary_backups_per_service</s:item>
                                    <s:item>max_remove_summary_s2_per_service</s:item>
                                    <s:item>max_replication_errors</s:item>
                                    <s:item>mode</s:item>
                                    <s:item>multisite</s:item>
                                    <s:item>notify_scan_min_period</s:item>
                                    <s:item>notify_scan_period</s:item>
                                    <s:item>peers</s:item>
                                    <s:item>percent_peers_to_reload</s:item>
                                    <s:item>percent_peers_to_restart</s:item>
                                    <s:item>precompress_cluster_bundle</s:item>
                                    <s:item>primary_rebalance_max_drift_percent</s:item>
                                    <s:item>primary_src_persist_secs</s:item>
                                    <s:item>quiet_period</s:item>
                                    <s:item>rcv_timeout</s:item>
                                    <s:item>re_add_on_bucket_request_error</s:item>
                                    <s:item>rebalance_pipeline_batch_size</s:item>
                                    <s:item>rebalance_primaries_execution_limit_ms</s:item>
                                    <s:item>rebalance_search_completion_timeout</s:item>
                                    <s:item>rebalance_threshold</s:item>
                                    <s:item>register_forwarder_address</s:item>
                                    <s:item>register_replication_address</s:item>
                                    <s:item>register_search_address</s:item>
                                    <s:item>remote_storage_retention_period</s:item>
                                    <s:item>remote_storage_upload_timeout</s:item>
                                    <s:item>rep_cxn_timeout</s:item>
                                    <s:item>rep_max_rcv_timeout</s:item>
                                    <s:item>rep_max_send_timeout</s:item>
                                    <s:item>rep_rcv_timeout</s:item>
                                    <s:item>rep_send_timeout</s:item>
                                    <s:item>replication_factor</s:item>
                                    <s:item>replication_port</s:item>
                                    <s:item>replication_use_ssl</s:item>
                                    <s:item>report_remote_storage_bucket_upload_to_targets</s:item>
                                    <s:item>reporting_delay_period</s:item>
                                    <s:item>restart_inactivity_timeout</s:item>
                                    <s:item>restart_timeout</s:item>
                                    <s:item>rolling_restart</s:item>
                                    <s:item>rolling_restart_condition</s:item>
                                    <s:item>search_factor</s:item>
                                    <s:item>search_files_retry_timeout</s:item>
                                    <s:item>searchable_rebalance</s:item>
                                    <s:item>searchable_rolling_peer_state_delay_interval</s:item>
                                    <s:item>secret</s:item>
                                    <s:item>send_timeout</s:item>
                                    <s:item>service_interval</s:item>
                                    <s:item>service_jobs_msec</s:item>
                                    <s:item>site</s:item>
                                    <s:item>site_by_site</s:item>
                                    <s:item>site_mappings</s:item>
                                    <s:item>site_replication_factor</s:item>
                                    <s:item>site_search_factor</s:item>
                                    <s:item>streaming_replication_wait_secs</s:item>
                                    <s:item>summary_registration_batch_size</s:item>
                                    <s:item>summary_replication</s:item>
                                    <s:item>summary_update_batch_size</s:item>
                                    <s:item>target_wait_time</s:item>
                                    <s:item>upload_rectifier_timeout_secs</s:item>
                                    <s:item>use_batch_mask_changes</s:item>
                                    <s:item>use_batch_remote_rep_changes</s:item>
                                </s:list>
                            </s:key>
                            <s:key name="requiredFields">
                                <s:list/>
                            </s:key>
                            <s:key name="wildcardFields">
                                <s:list/>
                            </s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="executor_workers">10</s:key>
                    <s:key name="forwarderdata_rcv_port">0</s:key>
                    <s:key name="forwarderdata_use_ssl">0</s:key>
                    <s:key name="frozen_notifications_per_batch">10</s:key>
                    <s:key name="guid">0F48E6FE-0412-4AB7-8F67-EDD22B89AD2B</s:key>
                    <s:key name="heartbeat_period">18446744073709551615</s:key>
                    <s:key name="heartbeat_timeout">60</s:key>
                    <s:key name="manager_switchover_idx_ping">1</s:key>
                    <s:key name="manager_switchover_mode">disabled</s:key>
                    <s:key name="manager_switchover_quiet_period">60</s:key>
                    <s:key name="manager_uri">?</s:key>
                    <s:key name="master_uri">?</s:key>
                    <s:key name="max_auto_service_interval">1</s:key>
                    <s:key name="max_delayed_updates_time_ms ">1000000</s:key>
                    <s:key name="max_fixup_time_ms">0</s:key>
                    <s:key name="max_peer_build_load">5</s:key>
                    <s:key name="max_peer_rep_load">5</s:key>
                    <s:key name="max_peer_sum_rep_load">5</s:key>
                    <s:key name="max_peers_to_download_bundle">0</s:key>
                    <s:key name="max_primary_backups_per_service">10</s:key>
                    <s:key name="mode">disabled</s:key>
                    <s:key name="multisite">false</s:key>
                    <s:key name="notify_buckets_period">10</s:key>
                    <s:key name="notify_scan_min_period">10</s:key>
                    <s:key name="notify_scan_period">10</s:key>
                    <s:key name="percent_peers_to_reload">100</s:key>
                    <s:key name="percent_peers_to_restart">10</s:key>
                    <s:key name="ping_flag">1</s:key>
                    <s:key name="precompress_cluster_bundle">1</s:key>
                    <s:key name="quiet_period">60</s:key>
                    <s:key name="rcv_timeout">60</s:key>
                    <s:key name="register_forwarder_address"></s:key>
                    <s:key name="register_replication_address"></s:key>
                    <s:key name="register_search_address"></s:key>
                    <s:key name="remote_storage_upload_timeout">60</s:key>
                    <s:key name="rep_cxn_timeout">5</s:key>
                    <s:key name="rep_max_rcv_timeout">600</s:key>
                    <s:key name="rep_max_send_timeout">600</s:key>
                    <s:key name="rep_rcv_timeout">10</s:key>
                    <s:key name="rep_send_timeout">5</s:key>
                    <s:key name="replication_factor">3</s:key>
                    <s:key name="replication_port"></s:key>
                    <s:key name="replication_use_ssl">0</s:key>
                    <s:key name="reporting_delay_period">10</s:key>
                    <s:key name="restart_timeout">60</s:key>
                    <s:key name="search_factor">2</s:key>
                    <s:key name="search_files_retry_timeout">600</s:key>
                    <s:key name="searchable_rolling_peer_state_delay_interval">60</s:key>
                    <s:key name="secret"></s:key>
                    <s:key name="send_timeout">60</s:key>
                    <s:key name="service_execution_threshold_ms">1500</s:key>
                    <s:key name="service_interval">1</s:key>
                    <s:key name="site">default</s:key>
                    <s:key name="streaming_replication_wait_secs">60</s:key>
                    <s:key name="summary_update_batch_size">10</s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
   ```
7. Get List of Deployment Client Configuration And Status
   - Example cURL:
   ```
    https://localhost:8089/services/deployment/client
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
  ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>deploymentclient</title>
        <id>https://localhost:8089/services/deployment/client</id>
        <updated>2023-12-19T11:16:46-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/deployment/client/listIsDisabled" rel="listIsDisabled"/>
        <opensearch:totalResults>1</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>config</title>
            <id>https://localhost:8089/services/deployment/client/config</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/services/deployment/client/config" rel="alternate"/>
            <author>
                <name>system</name>
            </author>
            <link href="/services/deployment/client/config" rel="list"/>
            <link href="/services/deployment/client/config" rel="edit"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">1</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app"></s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">0</s:key>
                            <s:key name="owner">system</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>splunk-system-role</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>splunk-system-role</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">0</s:key>
                            <s:key name="sharing">system</s:key>
                        </s:dict>
                    </s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
  ```
8. Access Lookup Table Files 
   - Example cURL:
   ```
    https://localhost:8089/services/data/lookup-table-files/
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>lookup-table-files</title>
        <id>https://localhost:8089/services/data/lookup-table-files</id>
        <updated>2023-12-19T11:18:00-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/data/lookup-table-files/_new" rel="create"/>
        <link href="/services/data/lookup-table-files/_reload" rel="_reload"/>
        <link href="/services/data/lookup-table-files/_acl" rel="_acl"/>
        <opensearch:totalResults>10</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
        <entry>
            <title>examples.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv" rel="list"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv" rel="edit"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv" rel="remove"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/examples.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">splunk-dashboard-studio</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\splunk-dashboard-studio\lookups\examples.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>firewall_example.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv" rel="list"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv" rel="edit"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv" rel="remove"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/firewall_example.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">splunk-dashboard-studio</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\splunk-dashboard-studio\lookups\firewall_example.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>geo_attr_countries.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv" rel="list"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv" rel="edit"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv" rel="remove"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_countries.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">search</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\search\lookups\geo_attr_countries.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>geo_attr_us_states.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv" rel="list"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv" rel="edit"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv" rel="remove"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_attr_us_states.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">search</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\search\lookups\geo_attr_us_states.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>geo_countries.kmz</title>
            <id>https://localhost:8089/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz" rel="list"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz" rel="edit"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz" rel="remove"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_countries.kmz/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">search</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\search\lookups\geo_countries.kmz]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>geo_us_states.kmz</title>
            <id>https://localhost:8089/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz" rel="list"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz" rel="edit"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz" rel="remove"/>
            <link href="/servicesNS/nobody/search/data/lookup-table-files/geo_us_states.kmz/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">search</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>power</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\search\lookups\geo_us_states.kmz]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>geomaps_data.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv" rel="list"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv" rel="edit"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv" rel="remove"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/geomaps_data.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">splunk-dashboard-studio</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\splunk-dashboard-studio\lookups\geomaps_data.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>outages_example.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv" rel="list"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv" rel="edit"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv" rel="remove"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/outages_example.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">splunk-dashboard-studio</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\splunk-dashboard-studio\lookups\outages_example.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>pura_mark_public_as_private.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv" rel="list"/>
            <link href="/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv" rel="edit"/>
            <link href="/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv" rel="remove"/>
            <link href="/servicesNS/nobody/python_upgrade_readiness_app/data/lookup-table-files/pura_mark_public_as_private.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">python_upgrade_readiness_app</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>sc_admin</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                            <s:item>sc_admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\python_upgrade_readiness_app\lookups\pura_mark_public_as_private.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
        <entry>
            <title>security_example_data.csv</title>
            <id>https://localhost:8089/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv</id>
            <updated>1969-12-31T19:00:00-05:00</updated>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv" rel="alternate"/>
            <author>
                <name>nobody</name>
            </author>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv" rel="list"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv/_reload" rel="_reload"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv" rel="edit"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv" rel="remove"/>
            <link href="/servicesNS/nobody/splunk-dashboard-studio/data/lookup-table-files/security_example_data.csv/move" rel="move"/>
            <content type="text/xml">
                <s:dict>
                    <s:key name="disabled">0</s:key>
                    <s:key name="eai:acl">
                        <s:dict>
                            <s:key name="app">splunk-dashboard-studio</s:key>
                            <s:key name="can_change_perms">1</s:key>
                            <s:key name="can_list">1</s:key>
                            <s:key name="can_share_app">1</s:key>
                            <s:key name="can_share_global">1</s:key>
                            <s:key name="can_share_user">0</s:key>
                            <s:key name="can_write">1</s:key>
                            <s:key name="modifiable">1</s:key>
                            <s:key name="owner">nobody</s:key>
                            <s:key name="perms">
                                <s:dict>
                                    <s:key name="read">
                                        <s:list>
                                            <s:item>*</s:item>
                                        </s:list>
                                    </s:key>
                                    <s:key name="write">
                                        <s:list>
                                            <s:item>admin</s:item>
                                        </s:list>
                                    </s:key>
                                </s:dict>
                            </s:key>
                            <s:key name="removable">1</s:key>
                            <s:key name="sharing">global</s:key>
                        </s:dict>
                    </s:key>
                    <s:key name="eai:appName">search</s:key>
                    <s:key name="eai:data">
                        <![CDATA[C:\Program Files\Splunk\etc\apps\splunk-dashboard-studio\lookups\security_example_data.csv]]>
                    </s:key>
                    <s:key name="eai:userName">caob</s:key>
                </s:dict>
            </content>
        </entry>
    </feed>
    ```
9.  Get A List Of Metric Names
    - Example cURL:
   ```
    https://localhost:8089/services/catalog/metricstore/metrics
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>metricstore-metrics</title>
        <id>https://localhost:8089/services/catalog/metricstore/metrics</id>
        <updated>2023-12-19T11:19:39-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <opensearch:totalResults>0</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
    </feed>
    ```
10. Returns rollup summaries and the metric indexes with which they are associated.
    - Example cURL:
   ```
    https://localhost:8089/services/catalog/metricstore/rollup
    --request GET \
    --user 'username':'password'
   ```
   - Response (XML)
    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xml" href="/static/atom.xsl"?>
    <feed xmlns="http://www.w3.org/2005/Atom" xmlns:s="http://dev.splunk.com/ns/rest" xmlns:opensearch="http://a9.com/-/spec/opensearch/1.1/">
        <title>metricstore_rollup</title>
        <id>https://localhost:8089/services/catalog/metricstore/rollup</id>
        <updated>2023-12-19T11:20:24-05:00</updated>
        <generator build="b6b9c8185839" version="9.1.2"/>
        <author>
            <name>Splunk</name>
        </author>
        <link href="/services/catalog/metricstore/rollup/_new" rel="create"/>
        <link href="/services/catalog/metricstore/rollup/_reload" rel="_reload"/>
        <link href="/services/catalog/metricstore/rollup/_acl" rel="_acl"/>
        <opensearch:totalResults>0</opensearch:totalResults>
        <opensearch:itemsPerPage>30</opensearch:itemsPerPage>
        <opensearch:startIndex>0</opensearch:startIndex>
        <s:messages/>
    </feed>
    ```
   
   
   


