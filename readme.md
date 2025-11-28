# EMA: The Universal AI Employee for Insurance Claims

![EMA Logo](frontend/public/Ema-full-logo-color.webp)

**EMA (Enterprise Multi-Agent Assistant)** is an autonomous, agentic AI system designed to revolutionize the insurance claims lifecycle. It moves beyond simple chatbots to act as a proactive "Universal AI Employee" that can execute complex workflows, analyze unstructured data, and make intelligent decisions.

---

## 🚨 The Problem: The "Claims Crisis"

Insurance claims are the moment of truth for customers, yet the backend process is often stuck in the past.

### 1. The "Swivel Chair" Effect
Adjusters spend **40-60% of their day** just moving data between systems. They toggle between emails, PDF invoices, policy documents, and legacy mainframes. This context switching kills productivity.

### 2. Unstructured Data Overload
Claims run on documents—handwritten notes, police reports, crash photos, and repair estimates. Traditional automation (RPA) breaks when it encounters this "messy" data, forcing humans to manually read and key in every line item.

### 3. Inconsistent Decision Making
With thousands of claims and hundreds of adjusters, consistency is impossible. One adjuster might approve a $500 bumper repair, while another rejects it based on a different interpretation of the same policy. This leads to **claims leakage** (overpayment) or unfair denials.

### 4. Slow Turnaround Time
Because of these bottlenecks, a simple auto claim can take **2-3 weeks** to settle. In the age of Amazon and Uber, customers expect instant resolution.

---

## 🧠 Our Approach: The "Universal AI Employee"

We didn't just want to build another "tool" for adjusters. We wanted to build a **teammate**.

### The Paradigm Shift
*   **Old Way (Tools)**: The human does the work, using software to record it.
*   **New Way (Agents)**: The AI does the work, and the human supervises it.

EMA is built on **Agentic Architecture**. It doesn't just wait for input; it proactively:
1.  **Observes**: Monitors the claims inbox for new FNOL (First Notice of Loss).
2.  **Thinks**: Uses LLMs to reason about coverage, liability, and fraud.
3.  **Acts**: Extracts data, updates databases, and drafts communications.

---

## ⚡ Current Prototype Capabilities

The current version of EMA is a fully functional prototype demonstrating the "Happy Path" of a high-tech claims workflow.

### 1. Autonomous Triage (FNOL)
*   **What it does**: Instantly ingests new claims.
*   **The Magic**: It analyzes the incident description and vehicle details to assign a **Risk Score** and **Severity Level** in milliseconds.
*   **Benefit**: High-risk claims are prioritized immediately.

### 2. Smart Document Analysis (Evidence Extractor)
*   **What it does**: Reads raw PDF repair estimates.
*   **The Magic**: Using GPT-4o, it extracts every line item (parts, labor, tax), identifies the vendor, and compares costs against policy limits.
*   **Benefit**: Turns "unstructured" PDFs into "structured" database records instantly.

### 3. Multi-Agent Reasoning
*   **What it does**: A team of specialized agents (Policy Interpreter, Fraud Detector) works in the background.
*   **The Magic**: Before a human even opens the file, EMA has already verified coverage and flagged potential fraud (e.g., "Labor rate > $100/hr").

### 4. Interactive Co-Pilot
*   **What it does**: A chat interface for the adjuster.
*   **The Magic**: You can ask, *"Why was this flagged?"* or *"Draft a rejection letter."* EMA has full context of the specific claim and policy.

---

## 🚀 Future Scope & Roadmap

We are building towards a fully autonomous claims organization.

### Phase 1: Enhanced Perception (Next Quarter)
*   **Computer Vision**: Analyze crash photos to automatically estimate repair costs (e.g., "Dented bumper = $800").
*   **Voice Agents**: AI that calls the customer to schedule an inspection or ask for missing details.

### Phase 2: Deep Integration (Year 1)
*   **Payment Rails**: Integration with Stripe/Zelle to issue instant payouts upon approval.
*   **Legacy Sync**: Two-way sync with Guidewire/Duck Creek to act as a modern layer on top of old systems.

### Phase 3: Autonomous Adjudication (Year 2+)
*   **Touchless Claims**: Simple claims (e.g., windshield cracks) are handled 100% by EMA without human intervention.
*   **Predictive Policy**: Using claims data to inform underwriting and pricing in real-time.

---

## 🏗️ Architecture

> **[Read the Full Architecture Deep Dive](ARCHITECTURE.md)**

*   **Frontend**: Next.js 14, Tailwind CSS
*   **Backend**: FastAPI, Python
*   **AI Orchestration**: LangGraph (Multi-Agent System)
*   **LLM**: Azure OpenAI (GPT-4o)
*   **Database**: Supabase

---

## 📦 Installation

1.  **Clone**: `git clone https://github.com/Kulraj69/ema.git`
2.  **Backend**:
    ```bash
    cd backend
    python -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    uvicorn main:app --reload
    ```
3.  **Frontend**:
    ```bash
    cd frontend
    npm install
    npm run dev
    ```

---

## 📄 License
MIT
