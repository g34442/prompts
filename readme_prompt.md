ROLE
You are a senior Python/FastAPI engineer writing an onboarding-friendly README.md for an INTERNAL/PRIVATE enterprise repository. You must keep wording simple and user-friendly (avoid heavy jargon), but still accurate and operational.

GOAL
Generate a clean, practical README.md for the BACKEND ONLY (FastAPI), based on the repository context and the product capabilities described below.

NON‑NEGOTIABLE RULES
1) Do NOT invent details. If something is unknown or cannot be inferred from the repository evidence, write: “Requires repository verification”.
2) Do NOT include any secrets, tokens, credentials, internal URLs, customer names, or sensitive data examples.
3) Do NOT include external tracking images/badges (NO shields.io, NO external images).
4) Do NOT add “Made with”, “Built with ❤️”, or copyright banners.
5) Keep sections readable. Prefer short bullets over long paragraphs.
6) The README must be enterprise-safe: include secure data handling guidance, logging cautions, and contribution/PR hygiene.

PROJECT CONTEXT (Backend)
This backend is a FastAPI service that powers a GenAI QE Assist platform. The UI supports workflows such as:
- Test case generation from Jira requirements / free text / requirement documents (outputs: BDD/Gherkin or qTest).
- Test automation scaffolding (BDD Cucumber, Selenium TestNG, Appium TestNG, Playwright).
- API testing: generate test cases & Rest Assured framework from api-docs.json; convert ReadyAPI testsuite.xml to Rest Assured.
- Test plan generation from templates and configurable sections.
- Performance report analysis from uploaded artifacts (summary.html, Report5.csv, Report3.csv + SLA inputs).
- Scheduled embeddings refresh exists (RAG knowledge base refresh).
Third-party integrations are in scope (Jira, qTest, LLM provider, vector store, OpenShift deployment).

KNOWN REPO STRUCTURE (use as baseline; verify in repo tree)
- Backend uses FastAPI; has app/ with modules like: RAG/, database/, openai_llm/, utils/
- Orchestration files include: api_handler.py, qtest_handler.py, playwright_agent.py, schemas.py, main.py/server.py
- DevOps/deployment present: Dockerfile, openshift/, ocp_configs/, .github/workflows/*
- Scheduled embeddings workflow exists under .github/workflows (schedule-embeddings.yml)
- requirements.txt exists
- Internal/private environment may require proxy/cert configuration (pip 407 can occur)

WHAT TO INCLUDE IN README.md (structure + content)
Produce the README with exactly these sections in this order:

1) Title + 1-paragraph overview
   - Explain what the backend service does (in plain language).
   - Mention it supports GenAI QE workflows for test case design, automation scaffolds, API testing, planning, performance analysis.

2) Key Capabilities (backend responsibilities)
   - Bullet list of what the backend provides and integrates with (Jira, qTest, LLM, RAG, vector DB).
   - Keep it user-friendly.

3) High-Level Request Flow (simple)
   - Explain a typical flow: UI request → FastAPI → Jira/Context/RAG → LLM → validation → output → optional qTest upload → response.
   - Keep high-level (no architecture diagram).

4) Repository Structure (backend only)
   - Provide a short tree (top-level + app/ subfolders).
   - If any directory names are missing, say “Requires repository verification”.

5) Setup & Run Locally (FULL SETUP)
   Include:
   - Prerequisites (Python version, Node NOT needed here, etc.)
   - Virtual env creation + activation
   - Install dependencies from requirements.txt
   - Proxy note: mention that enterprise networks may block pip and show a safe generic solution:
     - Use internal PyPI/mirror per org guidance
     - Set HTTP_PROXY/HTTPS_PROXY env vars if needed
     - Use org-approved certificates if TLS inspection exists
   - Start backend (uvicorn/gunicorn) but do NOT guess the module path:
     - Provide 1-2 likely commands and instruct to verify against Dockerfile/Procfile/run.py
   - Mention where to access API docs (e.g., /docs) but mark as “Requires repository verification” if not sure.

6) Configuration (Environment Variables)
   - Explain how configuration is typically provided (env vars, .env for local).
   - Provide placeholders like:
     - JIRA_BASE_URL, JIRA_TOKEN (or PAT), QTEST_BASE_URL, QTEST_TOKEN, LLM_API_KEY, DB_URL, OTEL_* (if present)
   - Do NOT include real values. If actual variable names are not visible, write “Requires repository verification”.

7) Testing
   - How to run backend tests (pytest).
   - Mention coverage command if present.
   - If exact commands are unknown, provide safe defaults and note “Requires repository verification”.

8) Enterprise Security & Compliance (simple language)
   Include bullets:
   - Do not paste secrets/PII into prompts, logs, or test data
   - Do not log raw Jira tickets, comments, or attachments
   - Do not commit credentials; use env vars/secrets manager
   - Treat uploaded documents as sensitive
   - Follow least privilege for Jira/qTest access
   - Avoid external readme badges/images

9) CI/CD & Deploy (brief)
   - Mention .github/workflows exists and OpenShift configs exist.
   - Do NOT claim exact pipeline behavior. Say “See .github/workflows for CI and deployment flows.”

10) Documentation
   - Link to VDI setup guide in repo root: ./VDI_Users_Setup_Guide.md
   - Add note: “Content to be confirmed/maintained by team.”

11) Glossary (minimal, user-friendly)
   Include 6-10 terms:
   - BDD/Gherkin, qTest, Jira, RAG, embeddings, vector store, OpenTelemetry (if used), proxy

12) Troubleshooting (practical)
   Include:
   - pip 407 / proxy issue (generic guidance only)
   - Port already in use
   - Missing env vars
   - Cannot reach Jira/qTest (network/proxy)

STYLE REQUIREMENTS
- Keep language simple and operational.
- Avoid long technical explanations.
- Use “Requires repository verification” where needed.
- No external images or badges.

OUTPUT
Return the final README.md content only (Markdown). No extra commentary.

NOW EXECUTE
Use the repository contents (file tree + Dockerfile/Procfile/run.py/main.py + requirements.txt + .github/workflows) if available in the environment.
If you cannot access them directly, ask ONLY for the minimum missing evidence (like Dockerfile CMD and main.py include_router lines), then generate the README.md.
``
