---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphchats "github.com/microsoftgraph/msgraph-sdk-go/chats"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



requestFilter := "teamsApp/id eq 'com.microsoft.teamspace.tab.web'"

requestParameters := &graphchats.ChatItemTabsRequestBuilderGetQueryParameters{
	Expand: [] string {"teamsApp"},
	Filter: &requestFilter,
}
configuration := &graphchats.ChatItemTabsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Chats().ByChatId("chat-id").Tabs().Get(context.Background(), configuration)


```