# n8n Full Beginner Course

This repository contains a comprehensive collection of n8n workflow projects, designed to help you learn automation and integration using n8n from beginner to advanced levels.

## Repository Structure

- `/*.json` - n8n workflow files for each project
- `/Google Sheets/` - CSV templates for Google Sheets integration
  - `Form Onboarding - responses.csv` - Template for form responses and email tracking
  - `RSS Feed - feed.csv` - Template for RSS Feed Trigger (1st Project)

## Course Projects

1. **RSS Feed Trigger** (Project 1)
   - Introduction to n8n Cloud
   - Working with RSS feeds
   - Integration with Google Sheets
   - Basic data transformation

2. **Logic Gmail** (Project 2)
   - Email automation with Gmail
   - Logic operations and conditional workflows
   - Data processing and filtering

3. **Basic LLM Chain** (Project 3)
   - Introduction to Language Model integration
   - Building AI-powered workflows
   - Chain operations and data processing

4. **Web Scraping HTTP Requests** (Project 4)
   - Web scraping fundamentals
   - Working with HTTP requests
   - Data extraction and processing
   - Integration with Airtable

5. **Vector Database AI Chatbot** (Project 5)
   - Advanced AI integration
   - Vector database operations
   - Building intelligent chatbots
   - Data persistence and retrieval

6. **Receipt Analyzer** (Project 6)
   - Frontend:
     - User interface for receipt submission
     - Form handling and data collection
     - Response visualization
   - Backend:
     - Document processing workflow
     - Data extraction from receipts
     - Backend automation and processing
     - Integration with frontend components

7. **Social Media Integration** (Project 7)
   - Multi-platform social media automation
   - Subflows for X (Twitter) and LinkedIn
   - Content generation and scheduling
   - Workflow modularity with subflows

8. **Telegram Google Calendar Assistant** (Project 8 & 9)
   - Telegram bot integration
   - Google Calendar automation
   - Building interactive assistants
   - Event management and scheduling

9. **MCP Integration** (Project 10)
   - Advanced server integration
   - Chatbot client implementation
   - System architecture and deployment

## Getting Started

1. Clone this repository
2. Import the workflows into your n8n instance
3. Configure the necessary credentials and API keys
4. Import CSV templates from the Google Sheets folder into your Google Sheets
5. Follow the project progression from 1 to 10

## Models used in these workflows were retired

Some workflows were exported with models that have since been shut down. They import fine, but the model node fails when it runs until you pick a current model in it:

| Workflow file | Node | Model in the file | Status | Pick instead |
| --- | --- | --- | --- | --- |
| `Project_3 Basic LLM Chain.json` | Anthropic Chat Model | `claude-3-7-sonnet-20250219` | retired 2026-02-19 | `claude-sonnet-5-5` |
| `Project_5 Vector Database AI Chatbot.json` | Anthropic Chat Model | `claude-3-7-sonnet-20250219` | retired 2026-02-19 | `claude-sonnet-5-5` |
| `Project_7 Social Media Generation.json` | Anthropic Chat Model | `claude-3-7-sonnet-20250219` | retired 2026-02-19 | `claude-sonnet-5-5` |
| `Project_7 LinkedIn Subflow.json` | Anthropic Chat Model | `claude-3-7-sonnet-20250219` | retired 2026-02-19 | `claude-sonnet-5-5` |
| `Project_7 X Subflow.json` | Anthropic Chat Model | `claude-3-7-sonnet-20250219` | retired 2026-02-19 | `claude-sonnet-5-5` |
| `Project_10 MCP Chatbot Client.json` | Anthropic Chat Model | `claude-3-7-sonnet-20250219` | retired 2026-02-19 | `claude-sonnet-5-5` |
| `Project_8&9 Telegram Google Calendar Assistant.json` | OpenAI Chat Model | `o3-mini` | shut down 2026-10-23 | `gpt-5.6-sol` |

The replacements are the ones Anthropic and OpenAI list on their deprecation pages ([Anthropic](https://docs.anthropic.com/en/docs/about-claude/model-deprecations), [OpenAI](https://developers.openai.com/api/docs/deprecations)).

To fix one: open the workflow, double-click the model node, and choose the new model from the **Model** list. Then save.

Project 6 (Receipt Analyzer) uses `gpt-4o`, which still works. OpenAI has announced that its GPT-4o snapshots (`gpt-4o-2024-08-06`, `gpt-4o-2024-11-20`) shut down on 2027-01-14, with `gpt-6-luna` as the replacement.

## Prerequisites

- Basic understanding of APIs and automation
- n8n instance (cloud or self-hosted)
- Required API keys and credentials for various services
- Google Workspace account for Sheets integration

## Notes

- Each project builds upon the knowledge from previous ones
- Projects are designed to showcase different aspects of n8n
- Credentials and sensitive data should be properly configured in your n8n instance
- CSV templates are provided for standardized data structure

## Helpful Resources

### General n8n Documentation
- [n8n Official Documentation](https://docs.n8n.io/)
- [n8n Academy](https://academy.n8n.io/)
- [n8n Community Forum](https://community.n8n.io/)
- [n8n Quickstart Guide](https://docs.n8n.io/try-it-out/)
- [Data Transformation Guide](https://docs.n8n.io/data/transforming-data/)

### Project-Specific Resources

#### Project 1: RSS & Google Sheets
- [RSS Node Documentation](https://docs.n8n.io/integrations/builtin/trigger-nodes/n8n-nodes-base.rssfeedreadtrigger/)
- [Google Sheets Integration](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.googlesheets/)
- [Working with JSON](https://docs.n8n.io/data/data-structure/)

#### Project 2: Gmail & Logic
- [Gmail Node Documentation](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.gmail/)
- [IF Node Guide](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.if/)
- [Switch Node Guide](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.switch/)

#### Project 3: LLM Integration
- [AI Nodes Overview](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.openai/)
- [HTTP Request Node](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.httprequest/)
- [Expression Editor Guide](https://docs.n8n.io/code-examples/expressions/)

#### Project 4: Web Scraping
- [HTTP Request Node Examples](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.httprequest/examples/)
- [Airtable Integration](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.airtable/)
- [HTML Extract Node](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.htmlextract/)

#### Project 5: Vector Database & AI
- [AI Nodes Documentation](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.openai/)
- [Webhook Node](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.webhook/)
- [Database Nodes](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.postgres/)

#### Project 6: Document Processing
- [Binary Data Handling](https://docs.n8n.io/data/binary-data/)
- [PDF Manipulation](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.pdf/)
- [OCR Integration](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.microsofttranslator/)

#### Project 7: Social Media
- [Twitter/X Integration](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.twitter/)
- [LinkedIn Node](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.linkedin/)
- [Subflows Guide](https://docs.n8n.io/workflows/subflows/)

#### Project 8 & 9: Telegram & Calendar
- [Telegram Node Documentation](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.telegram/)
- [Google Calendar Node](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.googlecalendar/)
- [Date & Time Helpers](https://docs.n8n.io/code-examples/expressions/dates/)

#### Project 10: MCP & Advanced Integration
- [Custom API Creation](https://docs.n8n.io/hosting/api/)
- [Error Handling](https://docs.n8n.io/workflows/error-handling/)
- [Security Best Practices](https://docs.n8n.io/hosting/security/)

### Additional Resources
- [n8n Blog](https://blog.n8n.io/)
- [n8n Use Cases](https://n8n.io/use-cases/)
- [API Authentication Guide](https://docs.n8n.io/integrations/authentication/)
- [Expression Syntax Guide](https://docs.n8n.io/code-examples/expressions/)
