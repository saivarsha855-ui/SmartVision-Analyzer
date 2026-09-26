# 🚀 SmartVision Analyzer

**SmartVision Analyzer** is an AI-powered career intelligence platform designed to help students, job seekers, and recruiters analyze resumes, understand career opportunities, identify skill gaps, and improve job readiness.

The platform combines **Machine Learning, Natural Language Processing, semantic matching, and interactive career analytics** to provide intelligent career-related insights.

---

## ✨ Features

| Feature                        | Description                                                   |
| ------------------------------ | ------------------------------------------------------------- |
| 📄 **Resume Analysis**         | Analyze resumes and extract relevant career information       |
| ✍️ **AI Resume Rewrite**       | Improve resume content using AI-powered suggestions           |
| 🎯 **ATS Resume Score**        | Evaluate resume compatibility with Applicant Tracking Systems |
| 🔎 **Job Description Matcher** | Compare resumes with job descriptions using semantic matching |
| 🗺️ **Career Roadmap**         | Generate personalized career development roadmaps             |
| 💻 **Portfolio Analyzer**      | Analyze portfolio and GitHub-related information              |
| 🤖 **AI Interview Simulator**  | Practice interview questions and receive evaluation           |
| 💰 **Salary Predictor**        | Predict salary ranges using machine learning                  |
| 🧩 **Skill Gap Analysis**      | Identify missing skills and receive recommendations           |
| 👥 **Recruiter Dashboard**     | Compare candidates and analyze candidate information          |
| 🔍 **Explainable AI**          | Provide explanations for selected ML predictions              |
| 📊 **Analytics Dashboard**     | Visualize career and user-related analytics                   |
| 🔐 **Authentication**          | Secure user registration and login using JWT                  |

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────────┐
                    │      SmartVision        │
                    │        Analyzer         │
                    └────────────┬────────────┘
                                 │
                    ┌────────────▼────────────┐
                    │      React Frontend     │
                    │ React 19 + Vite +       │
                    │ Tailwind CSS             │
                    └────────────┬────────────┘
                                 │
                              REST API
                                 │
                    ┌────────────▼────────────┐
                    │      FastAPI Backend     │
                    │ Authentication + Routes │
                    └────────────┬────────────┘
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                  │
      ┌───────▼───────┐  ┌──────▼──────┐  ┌──────▼──────┐
      │ ML Pipeline   │  │ NLP Pipeline│  │   Database  │
      │ Scikit-Learn  │  │ spaCy/BERT  │  │   SQLite    │
      └───────────────┘  └─────────────┘  └─────────────┘
```

---

## 🛠️ Technology Stack

### Frontend

* React 19
* Vite
* Tailwind CSS
* Framer Motion
* React Router
* JavaScript / JSX

### Backend

* Python 3.12+
* FastAPI
* Uvicorn
* Pydantic
* JWT Authentication

### Machine Learning & Analytics

* Scikit-Learn
* Random Forest
* Pandas
* NumPy
* Joblib

### Natural Language Processing

* spaCy
* Sentence Transformers
* BERT-based semantic matching
* PDFPlumber

### Database & Security

* SQLite
* JWT
* Python-JOSE
* Passlib / bcrypt

### Development & Deployment

* Git
* GitHub
* GitHub Actions
* Docker
* Docker Compose

---

## 📂 Project Structure

```text
SmartVision-Analyzer/
│
├── .github/
│   └── workflows/
│
├── backend/
│   ├── auth/
│   │   ├── auth_routes.py
│   │   ├── auth_utils.py
│   │   ├── oauth_store.py
│   │   ├── resume_history_db.py
│   │   └── user_db.py
│   │
│   ├── routes/
│   ├── ml_pipeline/
│   ├── utils/
│   ├── tests/
│   ├── main.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.*
│
├── .env.example
├── .gitignore
├── docker-compose.yml
├── render.yaml
├── netlify.toml
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
└── README.md
```

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/saivarsha855-ui/SmartVision-Analyzer.git
cd SmartVision-Analyzer
```

---

## 🐍 Backend Setup

Navigate to the backend:

```bash
cd backend
```

Create a virtual environment:

### Windows

```powershell
python -m venv venv
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
uvicorn main:app --reload
```

The backend will be available at:

```text
http://localhost:8000
```

FastAPI documentation:

```text
http://localhost:8000/docs
```

---

## 💻 Frontend Setup

Open a new terminal and navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will normally be available at:

```text
http://localhost:5173
```

---

## 🐳 Running with Docker

The project also includes Docker configuration.

Run:

```bash
docker-compose up --build
```

To stop the containers:

```bash
docker-compose down
```

---

## 🔌 API Endpoints

### Core APIs

| Method | Endpoint           | Purpose                      |
| ------ | ------------------ | ---------------------------- |
| POST   | `/analyze`         | Analyze resume information   |
| GET    | `/companies`       | Retrieve company information |
| GET    | `/metrics`         | Retrieve analytics metrics   |
| GET    | `/market-pulse`    | Retrieve market information  |
| POST   | `/evaluate-answer` | Evaluate an interview answer |

### Authentication APIs

| Method | Endpoint         | Purpose             |
| ------ | ---------------- | ------------------- |
| POST   | `/auth/register` | Register a new user |
| POST   | `/auth/login`    | Authenticate a user |

### Career Intelligence APIs

| Method | Endpoint                              | Purpose                           |
| ------ | ------------------------------------- | --------------------------------- |
| POST   | `/features/rewrite`                   | AI resume rewriting               |
| POST   | `/features/ats-score`                 | Calculate ATS score               |
| POST   | `/features/jd-match`                  | Match resume with job description |
| POST   | `/features/roadmap`                   | Generate career roadmap           |
| POST   | `/features/github-stats`              | Retrieve GitHub statistics        |
| POST   | `/features/portfolio-analyze`         | Analyze portfolio                 |
| POST   | `/features/interview/question`        | Generate interview questions      |
| POST   | `/features/interview/evaluate`        | Evaluate interview responses      |
| POST   | `/features/recruiter/compare`         | Compare candidates                |
| GET    | `/features/resume-builder/templates`  | Retrieve resume templates         |
| POST   | `/features/salary-predict`            | Predict salary                    |
| GET    | `/features/explain-predictions`       | Retrieve prediction explanations  |
| GET    | `/features/skill-gap-recommendations` | Generate skill recommendations    |
| GET    | `/features/user-analytics`            | Retrieve user analytics           |

---

## 🧠 Machine Learning Pipeline

SmartVision Analyzer uses multiple AI/ML techniques for career intelligence.

### Resume Intelligence

The system processes resume documents and extracts relevant information such as:

* Skills
* Experience
* Education
* Career-related information

### Semantic Matching

Sentence Transformer / BERT-based models are used to calculate semantic similarity between resume content and job descriptions.

### Salary Prediction

Machine learning models are used to estimate salary-related outcomes based on available career features.

### Skill Gap Analysis

The system compares existing candidate skills against expected job requirements and identifies potential skill gaps.

### Explainable AI

Selected predictions can be accompanied by explanations to help users understand the factors contributing to the model output.

---

## 🔐 Security

Sensitive local configuration files should **never be committed to the repository**.

The project uses environment variables and local configuration for sensitive information.

Examples of files that should remain local:

```text
.env
.env.local
backend/auth/.jwt_secret
*.db
*.sqlite
*.pkl
*.joblib
```

Always verify your changes before pushing them to GitHub.

---

## 🧪 Development Guidelines

Before submitting changes:

1. Run the backend locally.
2. Run the frontend locally.
3. Test the affected feature.
4. Check for console errors.
5. Verify API responses.
6. Make sure sensitive files are not tracked.
7. Commit only the required changes.

Example:

```bash
git status
git add .
git commit -m "Describe your changes"
git push
```

---

## 🤝 Contributing

Contributions are welcome.

To contribute:

1. Fork the repository.
2. Create a feature branch.

```bash
git checkout -b feature/your-feature
```

3. Make your changes.
4. Test the changes locally.
5. Commit your changes.

```bash
git commit -m "Add your feature"
```

6. Push your branch.

```bash
git push origin feature/your-feature
```

7. Open a Pull Request.

Please review the project's `CONTRIBUTING.md` and `CODE_OF_CONDUCT.md` before contributing.

---

## 📜 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for more information.

---

## 👩‍💻 Developer

**Sai Varsha**

GitHub:
https://github.com/saivarsha855-ui

Repository:
https://github.com/saivarsha855-ui/SmartVision-Analyzer

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

Thank you for checking out **SmartVision Analyzer**! 🚀
