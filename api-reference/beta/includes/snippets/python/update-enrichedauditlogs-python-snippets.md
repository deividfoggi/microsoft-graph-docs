---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

// THE PYTHON SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
client =  GraphServiceClient(request_adapter)

request_body = EnrichedAuditLogs()
request_body.@odata_type = '#microsoft.graph.networkaccess.enrichedAuditLogs'

sharepoint = EnrichedAuditLogsSettings()
sharepoint.@odata_type = 'microsoft.graph.networkaccess.enrichedAuditLogsSettings'


request_body.sharepoint = sharepoint
teams = EnrichedAuditLogsSettings()
teams.@odata_type = 'microsoft.graph.networkaccess.enrichedAuditLogsSettings'


request_body.teams = teams
exchange = EnrichedAuditLogsSettings()
exchange.@odata_type = 'microsoft.graph.networkaccess.enrichedAuditLogsSettings'


request_body.exchange = exchange



result = await client.network_access.settings.enriched_audit_logs.patch(request_body = request_body)


```