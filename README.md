**AI Mock Interview Workflow**

This repository contains an n8n workflow for conducting AI-powered mock interviews with resume parsing, audio transcription, and automated feedback delivery.

**Features**
- Resume Upload & Parsing – Extracts and embeds candidate resumes for personalized questions.
- Speech-to-Text Integration – Converts microphone audio into text using Deepgram API.
- Conversational AI – Powered by Google Gemini (PaLM) for interactive interview simulation.
- Contextual Memory – Uses Postgres + Supabase Vector Store for chat history and resume/job description retrieval.
- Automated Feedback – Sends detailed feedback to the candidate’s email after interview completion.
- Multi-Stage Interviews – Supports warmup, technical, behavioral, and techno-behavioral interview flows.
- Candidate responses are stored in Postgres and feedback is delivered via email.

**Steps followed**
- Import the workflow JSON file (AI_Interview_WithMicrophone_MUlti_Trial_latest.json) into n8n.
- Configure credentials for:
    Google Gemini (PaLM) API
    Postgres Database
    Supabase API
    Gmail (OAuth2)
    Deepgram API (for audio transcription)
- Deploy the webhooks:
   upload-resume → Handles resume uploads
   speech-to-text → Processes microphone audio
- Start your interview session via the frontend (resume + job description required).
