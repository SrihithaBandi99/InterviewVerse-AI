# InterviewVerse AI
### AI Powered Smart Interview Assessment: A Multi-Modal Framework for Automated Candidate Evaluation

InterviewVerse AI is an AI-powered recruitment and assessment platform designed to streamline candidate evaluation through resume screening, intelligent interview assessment, speech analysis, coding evaluation, and proctoring.

The platform combines multiple assessment modules to provide recruiters with structured candidate performance insights and help candidates understand their strengths and skill gaps.

## 🚀 Key Features

- **Resume Intelligence:** Analyzes uploaded resumes, identifies relevant skills, and evaluates alignment with selected job roles.
- **AI-Powered Interviews:** Evaluates candidate answers based on the interview question, skill, and difficulty level.
- **Speech Intelligence:** Supports speech transcription and speech analysis.
- **Coding Assessment:** Provides programming challenges and automated code evaluation.
- **Proctoring:** Supports assessment monitoring and integrity-related analysis.
- **Candidate Reports:** Consolidates assessment results into an overall performance report.
- **REST API:** Uses FastAPI to expose backend services and interactive API documentation.

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Backend | Python, FastAPI |
| API Documentation | Swagger UI, OpenAPI |
| Database | PostgreSQL / Supabase |
| Data Processing | Pandas, NumPy |
| AI and NLP | NLP and semantic matching techniques |
| Frontend | React, Vite |
| Version Control | Git, GitHub |
| Deployment Architecture | Vercel, Render, Supabase |

*The exact libraries and deployment services used may vary depending on the configured project environment.*

## 🏗️ System Architecture

The system follows a modular architecture:

1. **Presentation Layer:** Candidate and recruiter interfaces for uploading resumes, completing assessments, and viewing reports.
2. **Backend Layer:** FastAPI endpoints handle requests and coordinate assessment services.
3. **AI Assessment Layer:** Performs resume analysis, interview evaluation, speech processing, coding evaluation, and proctoring analysis.
4. **Data Layer:** Stores candidate information and assessment-related records using the configured database.
5. **Deployment Layer:** Supports frontend hosting, backend deployment, database services, and source-code management.

## 📂 Project Structure

```text
InterviewVerse-AI/
├── ai_engine/
├── backend/
│   └── app/
│       ├── api/
│       ├── models/
│       ├── schemas/
│       ├── services/
│       │   ├── amci_engine.py
│       │   ├── coding_service.py
│       │   ├── interview_service.py
│       │   ├── job_service.py
│       │   ├── proctoring_service.py
│       │   ├── results_service.py
│       │   ├── resume_service.py
│       │   └── speech/
│       ├── config/
│       └── main.py
├── datasets/
│   └── job_descriptions/
│       └── job_descriptions.csv
├── README.md
└── requirements.txt
```

*This is a representative structure based on the available project details. Your repository may contain additional files and directories.*

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.10 or a compatible version
- pip
- Git
- PostgreSQL or a configured Supabase database, if required
- Node.js and npm for the React frontend

### 1. Clone the Repository

```bash
git clone https://github.com/mahathi30093/InterviewVerse-AI.git
cd InterviewVerse-AI
```

### 2. Set Up the Python Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**
```bash
venv\Scripts\activate
```

**Linux / macOS**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Ensure that the required environment variables and database settings are configured before starting services that depend on them.

### 4. Start the Backend

From the project root, run:

```bash
python -m uvicorn app.main:app --reload --app-dir backend --port 8000
```

The backend should be available at:

- **API Base URL:** http://localhost:8000
- **Swagger Documentation:** http://localhost:8000/docs
- **OpenAPI Schema:** http://localhost:8000/openapi.json
- **Health Check:** http://localhost:8000/health

### 5. Start the Frontend

Navigate to the frontend directory containing `package.json` and run:

```bash
npm install
npm run dev
```

Use the local URL printed by Vite. The frontend API configuration should point to the running backend.

## 🔌 Core API Modules

The backend provides endpoints for the following assessment functions:

| Endpoint | Method | Purpose |
|---|---|---|
| `/health` | GET | Checks backend health |
| `/api/resume/analyze` | POST | Analyzes a resume against a job role |
| `/api/interview/evaluate` | POST | Evaluates an interview answer |
| `/api/speech/transcribe` | POST | Transcribes speech |
| `/api/speech/analyze` | POST | Analyzes speech |
| `/api/proctoring/analyze` | POST | Performs proctoring analysis |
| `/api/coding/submit` | POST | Submits a coding assessment |

Check the Swagger documentation at `/docs` for the actual request schemas, supported inputs, and available endpoints.

## 📊 Dataset Sources

The following datasets are relevant to the project's assessment modules. Confirm which datasets are downloaded, configured, and used by the current implementation.

| Dataset | Application |
|---|---|
| [Resume Dataset](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset) | Resume analysis and skill extraction |
| [Job Description Dataset](https://www.kaggle.com/datasets/ravindrasinghrana/job-description-dataset) | Job-role matching |
| [Mozilla Common Voice](https://mozilladatacollective.com/organization/cmh0l9o10006n0j7jd45h73k) | Speech recognition research |
| [RAVDESS](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio) | Speech emotion analysis research |
| [CodeSearchNet](https://github.com/github/CodeSearchNet) | Code-related NLP research |

Review each dataset's licence and usage conditions before redistribution or commercial use.

## 🧪 Testing and Validation

The backend can be checked using the health endpoint and interactive Swagger UI.

Recommended validation steps:

1. Verify that the backend starts successfully.
2. Check the health endpoint.
3. Test resume analysis with a supported resume file and job role.
4. Submit sample interview answers for evaluation.
5. Test speech endpoints with supported input formats.
6. Submit coding solutions and inspect the evaluation response.
7. Verify that assessment results are stored and retrieved correctly when database integration is enabled.

Test scores and sample screenshots should be treated as demonstrations unless supported by a documented evaluation methodology and experimental results.

## 🌟 Project Novelty

1. **Multi-Modal Assessment:** Combines resume screening, interview evaluation, speech analysis, coding assessment, and proctoring in a unified platform.
2. **Context-Aware Evaluation:** Evaluates candidate responses and resume skills in relation to job requirements rather than relying only on keyword matching.
3. **Integrated Reporting:** Consolidates assessment outcomes to support structured candidate comparison and reduce manual evaluation effort.

## 🔮 Future Scope

- Improve evaluation accuracy through larger, representative datasets.
- Add explainable scoring and evidence-based feedback.
- Evaluate fairness across candidate groups and job categories.
- Expand support for languages, programming tasks, and interview formats.
- Strengthen assessment security and privacy controls.
- Validate AI-generated scores against expert human assessments.
- Add recruiter analytics and configurable assessment criteria.

## ⚠️ Responsible Use

InterviewVerse AI is intended to support recruitment assessment, not replace human decision-making. Automated scores should be reviewed alongside relevant evidence and human judgment. Speech, emotion, and proctoring signals should not be treated as definitive evidence of a candidate's competence, honesty, or suitability. Candidate data should be handled securely and in accordance with applicable privacy requirements.

## 👥 Project Team

- **Vanjari Sai Dhanush** — 2420030162 (Team Lead)
- **Bandi Srihitha** — 2420030099
- **Emani Mahathi** — 2420030093

## 🔗 Repository

[GitHub — InterviewVerse AI](https://github.com/mahathi30093/InterviewVerse-AI)

## 📄 License

Add the project's chosen licence here after confirming the intended terms of use and distribution.

---

**InterviewVerse AI — Making candidate assessment more structured, intelligent, and efficient.**
