# HR Onboarding Agent for GlobalLogic

A declarative agent for Microsoft 365 Copilot that helps new GlobalLogic employees navigate their first 90 days — from setup to team introductions and benefits enrollment.

## What it does

- Provides first week onboarding checklists
- Guides through IT setup and development environment configuration
- Answers questions about company policies and benefits
- Helps new employees connect with the right people
- Sources information from HR SharePoint documents

## Prerequisites

- [Node.js](https://nodejs.org/) (v18, 20, or 22)
- [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts)
- [Microsoft 365 Agents Toolkit](https://aka.ms/teams-toolkit) v5.0.0+
- [Microsoft 365 Copilot license](https://learn.microsoft.com/microsoft-365-copilot/extensibility/prerequisites#prerequisites)

## Quick Start

1. Open the Microsoft 365 Agents Toolkit in VS Code
2. Sign in with your Microsoft 365 account
3. Select `Preview Local in Copilot (Edge)` or `Preview Local in Copilot (Chrome)`
4. Select the HR Onboarding Agent from Copilot
5. Ask questions like "What's my first week checklist?"

## Project Structure

| Path | Description |
|------|-------------|
| `appPackage/declarativeAgent.json` | Agent configuration and capabilities |
| `appPackage/instruction.txt` | Agent instructions and behavior rules |
| `appPackage/EmbeddedKnowledge/` | HR documents (gitignored - add your own) |
| `appPackage/manifest.json` | Teams app manifest |

## Configuration

### Knowledge Sources
The agent uses SharePoint/OneDrive documents configured in `declarativeAgent.json`. Update the `capabilities` section with your HR document URLs.

### Instructions
Customize agent behavior by editing `appPackage/instruction.txt`.

## Resources

- [Declarative Agents Documentation](https://aka.ms/teams-toolkit-declarative-agent)
- [Build Declarative Agents Guide](https://learn.microsoft.com/microsoft-365-copilot/extensibility/build-declarative-agents)
