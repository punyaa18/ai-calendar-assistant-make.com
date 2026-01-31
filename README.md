## AI Calendar Assistant — Make.com Automation

An AI-powered calendar automation built using Make.com, Google Gemini, OpenAI, and Google Calendar.

This system automatically converts natural language requests into real calendar events.

Example input:

“Schedule a meeting with John tomorrow at 5 PM”

The automation understands the intent, extracts event details using AI, creates the calendar event, and returns a smart confirmation response.

For more details, read the automation_details.md file    


## the workflow 
<img width="1365" height="644" alt="image" src="https://github.com/user-attachments/assets/c38b24c9-f4c5-4c1d-8aee-4286ede9bc3b" />

## Process Flowchart

```mermaid
graph TD
    A["Webhook Trigger<br/>User Input"] --> B["Google Gemini AI<br/>Extract Data"]
    B --> C["JSON Parsing<br/>Structured Format"]
    C --> D["Tools Module<br/>Format & Validate"]
    D --> E{Sufficient<br/>Information?}
    E -->|No| F["Request Clarification"]
    F --> A
    E -->|Yes| G["Google Calendar API<br/>Create Event"]
    G --> H["OpenAI ChatGPT<br/>Generate Response"]
    H --> I["Webhook Response<br/>Send Result"]
    I --> J["Success!"]
    
    style A fill:#e1f5ff
    style B fill:#f3e5f5
    style G fill:#c8e6c9
    style I fill:#fff9c4
    style J fill:#c8e6c9
```
