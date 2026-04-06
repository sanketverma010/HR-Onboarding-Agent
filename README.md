# HR Onboarding Agent

Helps new employees navigate their first 90 days — from setup to team introductions and benefits enrollment.

## What This Agent Does

- **Week 1 checklist**: Get your first week checklist as a new employee
- **Dev environment setup**: Learn how to set up your development environment
- **Who should I meet?**: Find out who to connect with in your first month
- **Benefits enrollment**: Learn how to enroll in company benefits
- **Company policies**: Access leave and time-off policies

## Knowledge Sources

This agent has access to:
- Onboarding Checklist
- Employee Benefits Guide
- IT Setup Guide
- Company Policies Summary

## Prerequisites

- [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts)
- [Microsoft 365 Agents Toolkit](https://aka.ms/teams-toolkit) v5.0.0+
- [Microsoft 365 Copilot license](https://learn.microsoft.com/microsoft-365-copilot/extensibility/prerequisites#prerequisites)

## Quick Start

1. Open the Microsoft 365 Agents Toolkit in VS Code
2. Sign in with your Microsoft 365 account
3. Select `Preview Local in Copilot (Edge)` or `Preview Local in Copilot (Chrome)`
4. Select the HR Onboarding Agent from Copilot
5. Start asking questions about onboarding

## Files

- `appPackage/declarativeAgent.json` - Agent configuration
- `appPackage/instruction.txt` - Agent instructions
- `appPackage/ai-plugin.json` - API plugin
- `appPackage/apiSpecificationFile/openapi.yaml` - API specification
- `appPackage/adaptiveCards/` - Response templates
- `appPackage/EmbeddedKnowledge/` - Knowledge documents
