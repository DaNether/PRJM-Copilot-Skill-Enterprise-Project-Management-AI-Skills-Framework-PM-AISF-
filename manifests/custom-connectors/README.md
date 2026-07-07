# Custom Connectors

**Version:** 1.0.0

Power Platform Custom Connector definitions for enterprise system integrations.

## Available Connectors

| Connector | System | Scope |
|-----------|--------|-------|
| azure-devops-connector.json | Azure DevOps | Read work items and sprint data |
| sharepoint-connector.json | SharePoint via Graph API | Read SharePoint lists and documents |

## Setup Instructions

1. Open [Power Platform Admin Centre](https://admin.powerplatform.microsoft.com).
2. Navigate to **Data → Custom Connectors**.
3. Select **New custom connector → Import an OpenAPI file**.
4. Upload the connector JSON file.
5. Configure authentication with your Azure AD app registration.
6. Test the connector with a known list/work item ID.

## Security Notes

- All connectors use OAuth 2.0 with Azure AD.
- Scopes are read-only by default.
- Store client secrets in Azure Key Vault — never in the connector definition.
