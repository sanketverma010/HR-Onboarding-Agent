# Declarative Agent for Microsoft 365 Copilot

A declarative agent template with custom knowledge sources and API plugin capabilities. This agent extends Microsoft 365 Copilot with domain-specific knowledge and actions through SharePoint integration and custom APIs.

## Capabilities

This declarative agent includes the following capabilities:

### 📚 Custom Knowledge Sources
- **SharePoint/OneDrive Integration**: Connect to SharePoint sites or OneDrive folders to provide the agent with domain-specific documents and knowledge
- **OneDrive for Business**: Reference specific files and folders from OneDrive for Business

### 🔌 API Plugin
- **Custom API Integration**: Extend agent capabilities with custom APIs defined through OpenAPI specifications
- **Adaptive Cards**: Rich UI responses using adaptive cards for structured data presentation
- **Custom Actions**: Enable the agent to perform specific actions through API endpoints

### 💡 Custom Instructions
- Define agent behavior and personality through custom instructions
- Set guidelines for how the agent should respond and interact with users

## Prerequisites

- [Node.js](https://nodejs.org/) (v18, 20, or 22)
- [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts)
- [Microsoft 365 Agents Toolkit](https://aka.ms/teams-toolkit) v5.0.0+
- [Microsoft 365 Copilot license](https://learn.microsoft.com/microsoft-365-copilot/extensibility/prerequisites#prerequisites)

## Quick Start

1. Open the Microsoft 365 Agents Toolkit in VS Code
2. Sign in with your Microsoft 365 account
3. Select `Preview Local in Copilot (Edge)` or `Preview Local in Copilot (Chrome)`
4. Select your declarative agent from Copilot
5. Start interacting with your agent

## Project Structure

| Path | Description |
|------|-------------|
| `appPackage/declarativeAgent.json` | Agent configuration and capabilities |
| `appPackage/instruction.txt` | Agent instructions and behavior rules |
| `appPackage/ai-plugin.json` | API plugin configuration |
| `appPackage/apiSpecificationFile/openapi.yaml` | OpenAPI specification for custom APIs |
| `appPackage/adaptiveCards/` | Adaptive card templates for API responses |
| `appPackage/EmbeddedKnowledge/` | Custom knowledge documents (add your own) |
| `appPackage/manifest.json` | Teams app manifest |

## Configuration

### Custom Knowledge Sources

Configure SharePoint/OneDrive knowledge sources in `declarativeAgent.json` under the `capabilities` section:

```json
"capabilities": [
  {
    "name": "OneDriveAndSharePoint",
    "items_by_url": [
      {
        "url": "https://yourtenant.sharepoint.com/sites/yoursite"
      }
    ]
  }
]
```

You can add multiple SharePoint sites, OneDrive folders, or specific file URLs.

### API Plugin

The API plugin is configured in two files:

1. **`ai-plugin.json`**: Defines the plugin metadata and authentication
2. **`apiSpecificationFile/openapi.yaml`**: OpenAPI 3.0 specification defining your API endpoints

To customize the API plugin:
- Update the OpenAPI spec with your API endpoints
- Configure authentication settings as needed
- Create adaptive cards in `appPackage/adaptiveCards/` for rich responses

### Agent Instructions

Customize agent behavior by editing `appPackage/instruction.txt`. Define:
- Agent's role and expertise
- Response style and tone
- Guidelines for using knowledge sources
- How to handle specific user queries

## Resources

- [Declarative Agents Documentation](https://aka.ms/teams-toolkit-declarative-agent)
- [Build Declarative Agents Guide](https://learn.microsoft.com/microsoft-365-copilot/extensibility/build-declarative-agents)
- [API Plugins for Copilot](https://learn.microsoft.com/microsoft-365-copilot/extensibility/overview-api-plugins)
- [Adaptive Cards](https://adaptivecards.io/)
