## What This Automation Does

Accepts user input via webhook

Uses AI to understand intent and extract structured data

Routes logic based on completeness of information

Creates Google Calendar events automatically

Sends intelligent confirmation messages back via webhook

## Example Use Cases

“Book a meeting with HR on Friday at 11 AM”

“Add client call tomorrow evening”

“Schedule standup meeting at 10 AM”

“Create a meeting with John next Monday”

## Tech Stack

**Make.com** – workflow orchestration

**Google Gemini AI** – natural language understanding

OpenAI (ChatGPT) – response generation

Google Calendar API

**Webhooks**

JSON parsing & routing logic

## 🔁 Flow Overview
## 1️⃣ Webhook Trigger

Receives natural language input from an external system or frontend.

Example:

{
  "message": "Schedule a meeting tomorrow at 5 PM with John"
}

## 2️⃣ Google Gemini AI

Processes the user message and extracts meaning such as:

intent

date

time

meeting title

participants

Converts unstructured text into structured information.

## 3️⃣ JSON Parsing

AI output is converted into structured fields usable inside the automation.

## 4️⃣ Tools Module

Used for:

formatting date & time

cleaning text

handling null or missing values

## 5️⃣ Router — Decision Logic

The router determines different paths based on AI output:

✅ sufficient information → create calendar event

❌ missing information → request clarification

This allows intelligent branching instead of fixed workflows.

## 6️⃣ Google Calendar Integration

Automatically creates events using extracted AI data:

event title

description

start time

end time

## 7️⃣ Iterator

Used for handling:

multiple outputs

scalable future logic

batch or recurring-like scenarios

## 8️⃣ OpenAI (ChatGPT)

Generates a natural, human-like confirmation message.

Example:

“Your meeting with John has been scheduled for tomorrow at 5 PM.”

## 9️⃣ Webhook Response

Final response is sent back to the calling system.

Example:

{
  "status": "success",
  "message": "Meeting scheduled successfully"
}



## Why This Project Matters

-This project demonstrates:  
-AI-driven automation design  
-Practical use of LLMs beyond chat  
-Real-world workflow engineering  
-Decision-based routing  
-Integration of multiple SaaS platforms  
-It reflects how AI systems are actually built in production, not just how prompts are written.  
 
## Future Enhancements

Conflict detection before scheduling  
Recurring meetings  
Timezone auto-detection  
WhatsApp / Slack integration  
Voice-based input  
Calendar availability checking  



## the final workflow   
<img width="1365" height="644" alt="image" src="https://github.com/user-attachments/assets/ac1456ff-8e20-4979-a637-ff04f8a6975a" />

