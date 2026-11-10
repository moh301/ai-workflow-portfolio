# AI Workflow Portfolio

Five workflows that connect chat, forms, data stores, and AI models for practical tasks. Each project includes the importable workflow and a short setup and verification guide.

| Project | What it does |
| --- | --- |
| [Real Estate Lead Assistant](real-estate-assistant.json) | Telegram agent that answers real estate inquiries with conversation context and can log leads to Google Sheets. |
| [Telegram Order Assistant](telegram-order-assistant.json) | Telegram ordering workflow that parses messages into structured data and uses routing rules to manage order records. |
| [AI Notification Agent](notification-agent.json) | Chat-based AI agent with memory and tools for sending notifications over Telegram and Pushover. |
| [Feedback Sentiment Router](feedback-sentiment.json) | Form-driven workflow that classifies feedback with an LLM and routes it based on structured output. |
| [Restaurant Order Workflow](restaurant-order-workflow.json) | Restaurant operations workflow that links an order form, Telegram interactions, and order records in Google Sheets. |

Import a workflow into n8n and follow its setup guide. Use synthetic data when trying integrations and reconnect credentials in your own workspace.

## Feedback Sentiment Router

Form-driven workflow that classifies feedback with an LLM and routes it based on structured output.

**Workflow:** Feedback form → OpenRouter LLM → structured output parser → Switch → Telegram on the connected branch.

## Run it in n8n

1. Import [feedback-sentiment.json](feedback-sentiment.json) into n8n.
2. Connect OpenRouter and Telegram. Configure the alert chat and check the Switch rules against the parser output.
3. Replace any remaining placeholders with your own test destinations before activation.

## Try it

Submit synthetic feedback in each category and verify the intended branch. Check what happens with an ambiguous response.

This is a portfolio workflow export. Credentials and pinned execution data are excluded, and integrations need to be configured in your own n8n instance.

## AI Notification Agent

Chat-based AI agent with memory and tools for sending notifications over Telegram and Pushover.

**Workflow:** n8n Chat Trigger → OpenRouter-backed AI agent with memory → Telegram or Pushover tool.

## Run it in n8n

1. Import [notification-agent.json](notification-agent.json) into n8n.
2. Connect OpenRouter, Telegram and Pushover. Set the Telegram chat ID and Pushover user key to destinations you control.
3. Replace any remaining placeholders with your own test destinations before activation.

## Try it

Request a harmless test message through each channel. Confirm the selected tool and recipient before using real destinations.

This is a portfolio workflow export. Credentials and pinned execution data are excluded, and integrations need to be configured in your own n8n instance.

## Real Estate Lead Assistant

Telegram agent that answers real estate inquiries with conversation context and can log leads to Google Sheets.

**Workflow:** Telegram → AI agent with OpenRouter and chat memory → Google Sheets lead tool → Telegram reply.

## Run it in n8n

1. Import [real-estate-assistant.json](real-estate-assistant.json) into n8n.
2. Connect Telegram, OpenRouter and Google Sheets. Select a test spreadsheet and match the lead columns in the append node.
3. Replace any remaining placeholders with your own test destinations before activation.

## Try it

Send a sample inquiry, then provide synthetic lead details. Verify that the reply stays relevant and the intended fields land in the sheet.

This is a portfolio workflow export. Credentials and pinned execution data are excluded, and integrations need to be configured in your own n8n instance.

## Restaurant Order Workflow

Restaurant operations workflow that links an order form, Telegram interactions, and order records in Google Sheets.

**Workflow:** Order form and Telegram triggers → JavaScript and routing → Google Sheets order lookups and updates → Telegram messages.

## Run it in n8n

1. Import [restaurant-order-workflow.json](restaurant-order-workflow.json) into n8n.
2. Connect Google Sheets and Telegram. Reselect each spreadsheet and tab, match column headers to the existing mappings, and configure test chats.
3. Replace any remaining placeholders with your own test destinations before activation.

## Try it

Submit a synthetic order, then exercise the Telegram actions and verify the sheet updates and messages. Use a test sheet for names and phone numbers.

This is a portfolio workflow export. Credentials and pinned execution data are excluded, and integrations need to be configured in your own n8n instance.

## Telegram Order Assistant

Telegram ordering workflow that parses messages into structured data and uses routing rules to manage order records.

**Workflow:** Telegram → Data Table lookup and routing → LLM parsing or JavaScript branch → Data Table update, sheet append, or Telegram reply.

## Run it in n8n

1. Import [telegram-order-assistant.json](telegram-order-assistant.json) into n8n.
2. Connect Telegram, OpenRouter and Google Sheets. Recreate and select the n8n Data Table using the lookup and write mappings. Reselect the destination spreadsheet and tab.
3. Replace any remaining placeholders with your own test destinations before activation.

## Try it

Use a test chat. Exercise the first message, a follow-up and the Google Sheets branch, and confirm each write affects the expected record.

This is a portfolio workflow export. Credentials and pinned execution data are excluded, and integrations need to be configured in your own n8n instance.

