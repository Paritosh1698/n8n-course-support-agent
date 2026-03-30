# Design to Live: Automated Agentic Workflow (n8n & Groq)

A high-velocity, production-ready conversational agent designed for **Course Selection Support**. This project demonstrates the "design-to-ship" cycle, moving from a blank canvas to a fully functional, safety-checked agentic workflow in record time using **n8n** and **Groq**.

<img width="1146" height="438" alt="Screenshot 2026-03-29 at 5 46 34 PM" src="https://github.com/user-attachments/assets/1fe9ecb3-d1c0-47b3-8daa-91a8e6c4cc78" />

---

## Overview

The **Course Selection Support Agent** bridges the gap between complex academic requirements and student inquiries. By pairing n8n’s powerful orchestration with the near-instant inference of Groq, this system provides a seamless, human-like experience while maintaining strict logic and safety standards.

---

## Key Features

* **Memory Management:** Implements persistent context to support natural, multi-turn conversations without losing track of user preferences or previous inputs.
* **Input Guardrails:** A logic-based safety layer that intercepts and handles "strong language" or out-of-scope queries before they reach the LLM.
* **Structured Output Parsing:** Automatically transforms raw LLM responses into predictable, structured data formats for reliable downstream integration.
* **Groq Inference:** Leverages high-speed inference to ensure zero-latency user experiences, even with complex agentic reasoning.
* **Autonomous Orchestration:** Uses n8n to manage the flow between user input, safety checks, and final response generation.

---

## Tech Stack

* **Orchestration:** n8n (Agentic Workflows)
* **Inference Engine:** Groq (Llama 4)
* **Logic & Safety:** n8n Expression Nodes
* **Deployment:** Production-ready n8n architecture

---

## Architecture

1.  **Trigger:** User submits a course-related query.
2.  **Safety Gate:** The **Input Guardrail** node scans for "strong language" or policy violations.
3.  **Context Retrieval:** The system pulls **Persistent Memory** to understand the user's academic history or preferences.
4.  **Inference:** **Groq** processes the prompt and generates a response.
5.  **Data Structuring:** The output is parsed into a structured format for a clean, consistent UI delivery.

---

## Setup & Deployment

1.  **Import:** Download the `Course Support.json` and import it into your n8n instance.
2.  **Credentials:**
    * Configure your **Groq API Key**.
    * (Optional) Connect your preferred chat interface (Telegram, Slack, or Webhook).
3.  **Configure Guardrails:** Customize the safety node to match your specific community guidelines.
4.  **Activate:** Deploy the workflow to start handling course selection inquiries.
