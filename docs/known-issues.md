---
title: Known Issues in Microsoft 365 Copilot Extensibility
description: Find information about current known issues related to Microsoft 365 Copilot extensibility and the recommended workarounds.
author: lauragra
ms.author: lauragra
ms.topic: concept-article
ms.date: 12/06/2024
---

# Known issues

This article provides information about known issues related to Microsoft 365 Copilot extensibility and any potential workarounds, if available.

## Declarative agents

The following known issues apply to declarative agents.

### Newly installed Copilot agents might not show in the Teams client right away

In some cases, a Copilot agent installed from the store doesn't immediately show up in Business Chat (BizChat) in the Teams client.

**Workaround:** The user can switch to another chat and then return to BizChat.

### Power Automate Flows aren't fully supported as actions in declarative agents

Power Automate Flows as actions in declarative agents might not run reliably and might not return results.

**Workaround:** Currently, no workaround for the issue that the flows might not return results is available. You can improve the trigger success for the flow by editing the description on the flow details page outside of Copilot Studio.

### Links are removed from Copilot responses

Copilot responses don't show links in the response body. Links are replaced with the following message: "An external link was removed to protect your privacy." 

This issue applies to links from any content source, including SharePoint, Microsoft Graph connectors, and plugins.

### Prompts to get a list based on custom metadata aren't supported 

Prompts to get a list of items based on custom metadata aren't supported. For example, the prompt "Get a list of ServiceNow tickets assigned to me" where "Assigned To" is based on custom metadata, doesn't work because the metadata isn't mapped to connection schema label properties.

**Workaround:** This issue doesn't currently have a workaround. You can get items based on matches with the title or description of the connector item.

### SharePoint knowledge search is limited

Currently when an agent searches a SharePoint site as a knowledge source, only files that are less than 512 MB are indexed and only the first 1000 characters are used.

###  Sharing links to SharePoint pages don't work as knowledge sources

When sharing links are references as a knowledge source in an agent, the agent doesn't return results from that knowledge source. The following is an example of a SharePoint sharing link:

'https://contoso.sharepoint-df.com**/:p:/r/**personal/babak_microsoft_com/Documents/'

### SharePoint files with special characters in the file name return no results

If a SharePoint file used as a knowledge source contains special characters in the file name, the agent returns no results based on that knowledge source.

### Pasting a link to a file in Copilot Studio and agent builder doesn't work

Currently, users can select a file in Copilot Studio and Copilot Studio agent builder and the agent will search the file. However, if the user pastes the URL of the file in prompt, the search fails.

**Workaround:** The user can select the file from the UI in Copilot Studio and Copilot Studio agent builder.

## Microsoft Graph connectors

The following known issues apply to Microsoft Graph connectors.

### Prompts to get items based on custom metadata aren't supported

Prompts to get a list of items based on custom metadata, such as "Get a list of ServiceNow tickets assigned to me" where "Assigned To" is custom metadata because it's not mapped to label properties of the connection schema, aren't supported.

## API plugins

The following known issues apply to API plugins.

### Some OpenAPI features aren't supported

The following OpenAPI features aren't supported for API plugins:

- Nested objects in API method request bodies or parameters.
- Polymorphic references (`oneOf`, `allOf`, `anyOf`) and circular references. As a workaround, use a flattened schema.
- API keys in custom headers, query parameters, or cookies.
- [OAuth grant flows](https://oauth.net/2/grant-types) other than vanilla Authcode and PKCE Authcode.
- Dual authentication flows (OAuth/Entra SSO + HTTP Bearer token) for a single API endpoint.
- Settings UI to reset always allow states. As a workaround, uninstall the app to reset the allow state.
- Settings UI to sign out. As a workaround, uninstall the app to reset the allow state or implement a function that the user can invoke using natural language.
- Multiple response semantics for a single function.
- **OpenURL** and **ToggleVisbility** adaptive card actions in response semantics.
- Task modules and stage views in response semantics.
