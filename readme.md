# EMA: The Universal AI Employee for Insurance Claims

EMA (Enterprise Multi-Agent Assistant) is an autonomous AI agent designed to revolutionize the insurance claims lifecycle. It acts as a "Universal AI Employee," capable of handling complex, multi-step workflows that traditionally require human intervention.

![EMA Dashboard](frontend/public/Ema-full-logo-color.webp)

## 🚀 Features

*   **Autonomous Claims Triage**: Instantly ingests First Notice of Loss (FNOL), analyzes severity, and assigns a risk score.
*   **Smart Document Analysis**: Uses Azure OpenAI (GPT-4o) to read unstructured documents (PDFs, invoices), extract line items, and validate costs against policy logic.
*   **Agentic Workflow**: A multi-agent system (built with LangGraph) that proactively verifies coverage, detects fraud, and drafts communication.
*   **Interactive Assistant**: A chat interface where adjusters can ask complex questions about claims, policies, or risks.
*   **Executive Analytics**: Real-time dashboard showing auto-approval rates, processing times, and cost savings.

## 🛠️ Tech Stack

### Frontend
*   **Framework**: Next.js 14 (App Router)
*   **Styling**: Tailwind CSS
*   **Icons**: Heroicons
*   **State Management**: React Hooks

### Backend
*   **Framework**: FastAPI (Python)
*   **AI Orchestration**: LangChain & LangGraph
*   **LLM**: Azure OpenAI (GPT-4o / GPT-4o-mini)
*   **Database**: Supabase (PostgreSQL) & Supabase Storage

## 📦 Installation

### Prerequisites
*   Node.js (v18+)
*   Python (v3.11+)
*   Supabase Account
*   Azure OpenAI Access

### 1. Clone the Repository
```bash
git clone https://github.com/Kulraj69/ema.git
cd ema
```

### 2. Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Create a `.env` file in the `backend` directory:
```env
AZURE_OPENAI_API_KEY=your_key
AZURE_OPENAI_ENDPOINT=your_endpoint
AZURE_OPENAI_API_VERSION=2024-08-01-preview
AZURE_OPENAI_DEPLOYMENT_NAME=gpt-4o-mini
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
```

Run the server:
```bash
uvicorn main:app --reload
```

### 3. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

Visit `http://localhost:3000` to see EMA in action.

## 🎬 Demo Flow

1.  **Dashboard**: View the "Claims Inbox" with pre-scored risks.
2.  **New Claim**: Click "+ New Claim" to simulate an FNOL intake.
3.  **Claim Detail**: Open a claim to see the "Agent Activity Log" (Evidence Extractor, Fraud Detector, etc.).
4.  **Document Analysis**: Click "View Policy Doc" -> "Analyze with AI" to see the LLM extract data from a raw invoice.
5.  **Assistant**: Use the chat to ask "Why was this flagged?" or "Draft an email to the customer."

## 📄 License
MIT
