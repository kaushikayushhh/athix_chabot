# athix_chabot
link: [https://kaushikayushh.app.n8n.cloud/webhook/de93928d-f006-4773-87ed-003110912271/chat]
This project is an AI-powered customer interaction automation workflow built using n8n and OpenAI.  The workflow receives user messages through a chat trigger and uses an AI agent to answer questions related to Athix
It retrieves information from Google Sheets for company details and FAQs, and stores user contact information if the AI cannot answer the query.

This system automates customer support and lead collection.

**2. Workflow Architecture**

The workflow consists of the following components:

Chat Trigger

AI Agent

OpenAI Language Model

Memory Buffer

Google Sheets Tools

The workflow processes user queries and either:

answers questions from stored knowledge

or saves the user's contact details for follow-up.

**3. Workflow Process**

Step 1 – Chat Trigger

The workflow starts when a user sends a message through the chat interface.

Node Used:

When chat message received

This node acts as a webhook that captures incoming messages.

Step 2 – AI Agent Processing

The message is passed to the AI Agent which analyzes the query and decides how to respond.

System behavior defined:

Answer questions about Athix.

Retrieve information from data sheets.

If no answer is found, collect the user's name and phone number.

Step 3 – AI Model

The AI Agent uses OpenAI chat model to generate responses.

Model used:

gpt-5-mini

This model processes user queries and produces conversational responses.

Step 4 – Memory Buffer

The workflow stores recent conversation history using a Simple Memory Buffer.

Function:

Keeps the last 10 messages in memory.

Maintains conversation context.

Step 5 – Knowledge Base (Google Sheets)

The workflow connects to Google Sheets as a knowledge base.

Two sheets are used:

Details Sheet

Contains company or product information.

**Purpose:**

AI retrieves company details when users ask about Athix.

FAQ Sheet

Contains frequently asked questions.

**Purpose:**

AI checks this sheet to answer common user queries.

Step 6 – Lead Collection

If the AI cannot answer the question, it collects:

Name

Phone Number

These details are stored in the Contact Sheet inside Google Sheets.

The workflow uses Append or Update functionality to store or update records.

**5. Technologies Used**

n8n – Workflow automation

OpenAI – Natural language AI model

Google Sheets – Knowledge base and data storage

Webhooks – Chat trigger

AI Agents – Decision making

**6. Key Features**

AI-powered customer support automation

Dynamic FAQ response system

Multi-language response capability

Conversation memory management

Automatic lead collection

Google Sheets integration for knowledge storage
