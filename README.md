# (18) AI-Powered-Speech-Analytics-for-Call-Centers
Call Analytics Pipeline – Audio → Transcript → AI Analysis → CSV Report → DOCX Report
This project automates the entire call-analysis workflow, starting from raw audio files and ending with a structured multi-format report. It is designed for customer support analytics, sentiment detection, and summarization.

# Project Workflow
1. Input

.m4a call recordings

Example: call1.m4a, call2.m4a, call3.m4a

2. Transcription (AssemblyAI / Whisper)

Each audio file is converted into a structured transcript JSON:

call1.json
call2.json
call3.json

3. AI Call Analysis

The transcripts are analyzed using an LLM to extract:

Customer Name

Agent Name

Sentiment

Issue Type

Call Summary

Output: callX_analysis.json

Example:

call1_analysis.json
call2_analysis.json
call3_analysis.json

4. CSV Report

All analysis JSON files are combined into a master CSV:

reports/all_calls_report.csv


Columns include:

File Name

Customer Name

Agent Name

Sentiment

Issue Type

Summary

5. DOCX Report

A formatted Word report is generated:

reports/Call_Analytics_Report.docx

# Project Structure
>> project/
│
├── data/
│   ├── call1.m4a
│   ├── call2.m4a
│   ├── call3.m4a
│   ├── call1.json
│   ├── call2.json
│   ├── call3.json
│   ├── call1_analysis.json
│   ├── call2_analysis.json
│   ├── call3_analysis.json
│
├── scripts/
│   ├── transcribe_audio.py
│   ├── analyze_transcript.py
│   ├── generate_csv.py
│   ├── generate_docx_report.py
│
├── reports/
│   ├── all_calls_report.csv
│   ├── Call_Analytics_Report.docx
│
└── README.md

# Features

✔ Automated audio → text transcription
✔ LLM-based call analysis
✔ JSON-structured outputs
✔ Combined CSV analytics
✔ DOCX report generation
✔ Easy to extend & integrate

# Technologies Used

Python

AssemblyAI (or Whisper) – transcription

Google Gemini / OpenAI – call analysis

Pandas – CSV creation

python-docx – report generation

# How to Run

Install dependencies:

pip install -r requirements.txt


Add your API keys inside the scripts:

AssemblyAI

Gemini/OpenAI

Run the pipeline:

python scripts/transcribe_audio.py
python scripts/analyze_transcript.py
python scripts/generate_csv.py
python scripts/generate_docx_report.py

# Output Preview
CSV Example
file	customer_name	agent_name	sentiment	issue_type	summary
DOCX Example

Executive Summary

Call-wise Analysis

Sentiment Insights

Customer Issues Breakdown
