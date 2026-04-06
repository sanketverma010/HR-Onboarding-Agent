# Declarative Agent for Microsoft 365 Copilot

A declarative agent that extends Microsoft 365 Copilot with custom capabilities.

## Capabilities

### OneDrive and SharePoint Integration
The agent can access documents from OneDrive and SharePoint to provide domain-specific knowledge. Files are referenced by URL in the agent configuration.

### API Actions
The agent includes custom API actions defined through an OpenAPI specification:
- **API Plugin** (`ai-plugin.json`) - Defines the plugin metadata and capabilities
- **OpenAPI Specification** (`openapi.yaml`) - Defines available API endpoints and operations
- **Adaptive Cards** - Provides rich UI responses for API results

### Conversation Starters
Pre-configured prompts help users quickly interact with the agent and discover its capabilities.

### Custom Instructions
The agent follows custom instructions defined in `instruction.txt` that guide its behavior and responses.

### Disclaimer
The agent displays a disclaimer to users about its intended use and limitations.

## Prerequisites

- [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts)
- [Microsoft 365 Agents Toolkit](https://aka.ms/teams-toolkit) v5.0.0+
- [Microsoft 365 Copilot license](https://learn.microsoft.com/microsoft-365-copilot/extensibility/prerequisites#prerequisites)

## Quick Start

1. Open the Microsoft 365 Agents Toolkit in VS Code
2. Sign in with your Microsoft 365 account
3. Select `Preview Local in Copilot (Edge)` or `Preview Local in Copilot (Chrome)`
4. Select the declarative agent from Copilot
5. Start interacting with the agent

## Project Structure

| File | Description |
|------|-------------|
| `appPackage/declarativeAgent.json` | Main agent configuration with capabilities and actions |
| `appPackage/instruction.txt` | Custom instructions for agent behavior |
| `appPackage/ai-plugin.json` | API plugin configuration |
| `appPackage/apiSpecificationFile/openapi.yaml` | OpenAPI specification for API actions |
| `appPackage/adaptiveCards/` | Adaptive card templates for rich responses |
| `appPackage/EmbeddedKnowledge/` | Knowledge source documents |
