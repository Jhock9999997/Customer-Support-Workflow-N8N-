# Customer-Support-Workflow-N8N-
This workflow listens for incoming emails in Gmail, classifies them, and intelligently handles customer support queries using an AI agent and a knowledge base

<img width="2230" height="690" alt="image" src="https://github.com/user-attachments/assets/3a18c125-a993-48be-b605-c58ba694305e" />

Workflow Overview
This workflow monitors your Gmail inbox for new emails, classifies their content, and intelligently processes customer support requests using an AI agent and contextual retrieval from a knowledge base.

Step-by-Step Process
1. Gmail Trigger
The workflow begins with a Gmail trigger that continuously watches the inbox for newly received messages.

2. Text Classification
Incoming emails are sent to a text classifier powered by an OpenAI model. Based on content analysis, emails are categorized into “Customer Support” or “Other”.
<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/a50d22ab-705c-46cc-bd4a-844df5d0eeeb" />


3. Conditional Logic
The flow splits depending on the classification result:

A) Customer Support Emails

The email is forwarded to an OpenAI Chat Model connected to an AI Agent.

The AI Agent uses a vector-based knowledge base (via OpenAI embeddings) to provide context-aware responses.

A label is added to the original email to help with inbox organization.

The AI then formulates and sends a reply through Gmail.

B) Non-Support Emails

These are passed through a “No Operation” node, which ends the workflow without further processing.

Key Components
- Gmail Trigger: Monitors incoming messages in real time.

- Text Classifier (OpenAI): Categorizes emails using natural language understanding.

- AI Agent: Utilizes OpenAI’s chat capabilities and a vector database to generate intelligent responses.

- Knowledge Base: Stores context-rich embeddings to support accurate information retrieval.

- Gmail Actions: Adds labels to categorize messages and sends automated replies.

Example: AI-Powered Customer Support Response
The screenshot above demonstrates a successful interaction between the AI agent and an incoming customer support email. When a user submitted the inquiry “Hi what times are yall open!!??”, the workflow extracted the message using dynamic referencing from the Gmail trigger node. The AI agent processed the message and returned a professional, informative response outlining business hours, communication channels, and a friendly sign-off. This illustrates the system's ability to accurately interpret informal language and generate helpful, human-like replies using contextual awareness.

<img width="3022" height="802" alt="image" src="https://github.com/user-attachments/assets/a69ebb1c-3e6f-47d5-aa93-9910bc45dae3" />

