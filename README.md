AI Log Analyzer

A containerized AI-powered DevOps log analysis application built with Flask, Docker, Docker Compose, Ollama, and Qwen2.5-Coder 3B.

The application analyzes Jenkins, Docker, Kubernetes, Linux, and application logs locally and provides AI-assisted troubleshooting insights.

Architecture
User
 |
 v
Flask AI Log Analyzer
 |
 | Docker Network
 v
Ollama
 |
 v
Qwen2.5-Coder 3B

Tech Stack
Python / Flask
Docker & Docker Compose
Ollama
Qwen2.5-Coder 3B
HTML / CSS / JavaScript
Gunicorn

Key Features
Automatic log-source detection
Error, warning, and information statistics
Repeated error detection
Sensitive-data masking
Local AI-powered log analysis
Root-cause and troubleshooting guidance
Safety filtering of AI recommendations
Downloadable analysis report
    
Setup
1. Clone the repository
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd ai-log-analyzer
2. Validate
python3 -m py_compile app.py
docker compose config
3. Build and start
docker compose up -d --build
4. Download the AI model
docker compose exec ollama ollama pull qwen2.5-coder:3b
5. Verify
docker compose ps
docker compose exec ollama ollama list
curl http://localhost:5001/health
6. Open the application
http://localhost:5001

Paste a log, select the source or use Auto, and click Analyze Log.

Analysis Flow

Log Input
   ↓
Sensitive Data Masking
   ↓
Source Detection
   ↓
Statistics
   ↓
Ollama / Qwen2.5-Coder
   ↓
Safety Validation
   ↓
AI Analysis


Security

The application masks common passwords, tokens, API keys, connection strings, and other sensitive values before sending logs to the local AI model. AI-generated recommendations should be reviewed before applying any command or configuration change.
