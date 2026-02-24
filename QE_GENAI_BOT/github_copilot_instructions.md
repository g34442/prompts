You are a principal software architect, enterprise systems auditor, and expert prompt engineer.
Context: I am a junior developer onboarding into an enterprise project with:
	• Backend: FastAPI
	• Frontend: Angular 14 + Bootstrap 5
	• Separate repositories
	• Enterprise environment
	• New project (not legacy)
	• DevOps configuration files present
Your task is NOT to give generic explanations. Your task is to produce a structured, actionable onboarding and architecture analysis framework specifically optimized for enterprise-grade FastAPI + Angular systems.
Avoid speculation. If something cannot be inferred from repository evidence, mark it as “requires repository verification.”

SECTION 1 – Enterprise Codebase Entry Strategy
Provide:
	1. A prioritized 7-step entry strategy for analyzing a new enterprise repository.
	2. A pattern recognition checklist to detect:
		○ Clean Architecture
		○ Hexagonal Architecture
		○ Layered (N-Tier)
		○ DDD-inspired modularity
	3. A cross-cutting concerns audit framework:
		○ Logging
		○ Error handling
		○ Authentication
		○ Validation
		○ Observability
		○ Configuration management
Output format:
	• Checklist
	• Decision-tree style reasoning
	• Risk indicators

SECTION 2 – FastAPI Enterprise Audit Framework
For each below category:
	• What to inspect
	• What good enterprise structure looks like
	• Red flags

Provide a deep audit model covering:
	1. Folder-to-responsibility mapping
	2. Dependency injection patterns
	3. Router grouping strategy
	4. Service layer abstraction analysis
	5. ORM integration (SQLAlchemy / Tortoise)
	6. Pydantic v2 schema usage patterns
	7. Auth implementation (OAuth2 / JWT / LDAP)
	8. Middleware layering
	9. Transaction boundaries
	10. Exception handling consistency
	11. Logging & monitoring hooks
	12. Test structure maturity

SECTION 3 – Angular 14 Enterprise Audit Model
Provide structured analysis covering:
	1. Feature-based modularization strategy
	2. Core vs Shared module responsibilities
	3. State management approach comparison:
		○ NgRx
		○ Akita
		○ RxJS service-based
	4. Interceptor responsibilities (auth, logging, retry)
	5. Guard patterns (role-based, token-based)
	6. Bootstrap 5 integration patterns
	7. Environment separation strategy
	8. Build optimization configuration
	9. End-to-end UI event tracing framework
For each category:
	• What to inspect
	• Architectural intent
	• Red flags

SECTION 4 – DevOps & Infrastructure Analysis
Provide a practical inspection model for:
	1. Dockerfile optimization patterns (backend & frontend)
	2. Multi-stage builds
	3. CI/CD YAML structure analysis
	4. Artifact versioning strategy
	5. Branch-to-environment mapping
	6. Secrets management
	7. Infrastructure-as-Code presence
	8. Deployment strategy (container registry → orchestration)
Output:
	• Commit-to-production lifecycle breakdown
	• Deployment maturity evaluation checklist

SECTION 5 – Persona-Based Evaluation Matrix
For each persona:
	• Architect
	• Backend Lead
	• Frontend Lead
	• DevOps Engineer
	• Product Manager
Provide:
	1. Primary evaluation focus
	2. Key technical questions
	3. Documentation artifacts they produce
	4. Risk lens they apply
	5. Decision criteria
Present as a comparison matrix.

SECTION 6 – End-to-End Request Trace Framework
Provide a deterministic tracing method for:
UI Event → Angular Component → Service → Interceptor → HTTP Client → FastAPI Router → Dependency → Service Layer → ORM → Database → Response → UI Update
Include:
	• File mapping strategy
	• Debug strategy
	• Logging inspection strategy

SECTION 7 – LLM-Based Repository Analysis Strategy
Research and synthesize:
	1. Prompt design principles for large repository analysis
	2. Techniques to prevent hallucination
	3. Structured output enforcement
	4. Progressive prompt chaining strategy
	5. Context window management strategies
	6. Verification prompts

SECTION 8 – Final Deliverables
Generate:
	1. A repeatable enterprise onboarding playbook
	2. A checklist-based evaluation framework
	3. A structured GitHub Copilot prompt library including:
		○ Backend audit prompt
		○ Frontend audit prompt
		○ DevOps audit prompt
		○ Architecture mapping prompt
		○ Risk analysis prompt
		○ End-to-end trace prompt
given prompts response must be:
	• Structured
	• Professional
	• Operational
	• Suitable for enterprise IT services environments
	• Free from unsupported assumptions
![Uploading image.png…]()
