# Multi-Agent Research System

A modular multi-agent research platform built with **Python** and **FastAPI**.

The system separates a research workflow into specialized agents:

- Planner Agent
- Researcher Agent
- Reviewer Agent
- Report Writer Agent

This repository is designed as a clean portfolio project that can later be connected to real LLM providers, web search, vector databases, and external tools.

## Features

- Multi-agent orchestration
- Research planning
- Structured research questions
- Research execution layer
- Review / validation layer
- Final report generation
- FastAPI REST API
- Docker support
- Unit and API tests
- Clean modular architecture

## Architecture

```text
User Request
    |
    v
Planner Agent
    |
    v
Researcher Agent
    |
    v
Reviewer Agent
    |
    v
Report Writer Agent
    |
    v
Final Research Report
```

## Project Structure

```text
multi-agent-research-system/
├── app/
│   ├── agents/
│   │   ├── planner.py
│   │   ├── researcher.py
│   │   ├── reviewer.py
│   │   └── writer.py
│   ├── main.py
│   └── orchestrator.py
├── tests/
│   └── test_api.py
├── .env.example
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── Makefile
├── requirements.txt
└── README.md
```

## Run Locally

```bash
python -m venv .venv
pip install -r requirements.txt
uvicorn app.main:app --reload
```

Open the interactive API docs at:

```text
http://127.0.0.1:8000/docs
```

## Example Request

```bash
curl -X POST "http://127.0.0.1:8000/research"   -H "Content-Type: application/json"   -d '{"topic":"agentic AI systems"}'
```

## Example Workflow

The planner creates research questions.

The researcher gathers or generates findings.

The reviewer validates the results.

The writer produces a final structured report.

## Production Upgrade Ideas

- OpenAI / Anthropic / Gemini integration
- Tavily / SerpAPI / browser-based research tools
- Vector database memory
- Source citations
- Tool calling
- Async task execution
- Human-in-the-loop review
- Long-term research memory
- Observability and tracing
- Prompt and output evaluation
- Authentication and rate limiting

## Resume / Portfolio Description

> Built a modular multi-agent research platform using Python and FastAPI with specialized planner, researcher, reviewer, and report-generation agents orchestrated through a clean production-style workflow.

## License

MIT
