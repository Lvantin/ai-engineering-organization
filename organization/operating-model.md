# AI Engineering Organization (AIEO) — Operating Model

**Version:** 1.1.0  
**Status:** Draft  
**Last Updated:** 2026-11-02

## 1. Purpose

This document defines how AIEO operates across projects, including organizational structure, Role governance, project configuration, Agent execution, engineering workflows, collaboration, quality management, and human oversight.

It establishes a consistent operating model while allowing each project to choose its architecture, Skills, Capabilities, and Technology Stack.

## 2. Operating Model Overview

AIEO operates through three layers.

### 2.1 Organization Layer

Responsible for:

- Defining and governing Roles.
- Maintaining reusable Skills and Capabilities.
- Defining Agent behavior and permissions.
- Publishing engineering standards and workflows.
- Managing Quality Gates and governance policies.
- Releasing versioned Organization capabilities.

### 2.2 Project Layer

Responsible for:

- Defining project objectives and requirements.
- Describing system architecture and components.
- Declaring Technology Stack.
- Selecting required Skills and Capabilities.
- Configuring project-specific workflows and constraints.
- Pinning the AIEO version.
- Managing project backlog and delivery.

### 2.3 Runtime Layer

Responsible for:

- Creating Agent instances.
- Assigning work.
- Executing tasks.
- Coordinating parallel activities.
- Performing reviews and testing.
- Producing engineering deliverables.

## 3. Organization Structure

### 3.1 Human Project Owner

Owns business direction, project objectives, and decisions requiring human authority.

Responsibilities:

- Define or approve business objectives.
- Resolve business-level conflicts.
- Approve high-impact decisions.
- Review project outcomes.
- Provide business acceptance.

### 3.2 Engineering Manager Agent

The primary project execution coordinator.

Responsibilities:

- Coordinate the project engineering workflow.
- Work with Product Manager to translate priorities into executable work.
- Manage execution priority and dependencies.
- Decompose work into tasks.
- Assign tasks to approved Roles.
- Instantiate Agent instances when needed.
- Coordinate parallel execution.
- Monitor progress, risks, and Quality Gates.
- Escalate issues requiring human or specialist decisions.
- Ensure engineering deliverables are complete and traceable.

The Engineering Manager does not override the Product Manager's business priority ownership or the Solution Architect's technical architecture ownership.

The Engineering Manager may instantiate only Roles approved and defined by the Organization.

### 3.3 Product Manager Agent

Owns business requirements and business priority.

Responsibilities:

- Gather and clarify requirements.
- Maintain the product backlog.
- Define business value and acceptance criteria.
- Prioritize backlog items.
- Coordinate business validation.
- Manage requirement changes.

The Product Manager owns business priority. The Engineering Manager owns execution priority, task sequencing, and technical dependencies.

### 3.4 Solution Architect Agent

Owns technical architecture and solution design.

Responsibilities:

- Understand business and non-functional requirements.
- Define system architecture.
- Identify application and service boundaries.
- Define integration patterns and contracts.
- Define data ownership and architectural constraints.
- Evaluate technical alternatives.
- Maintain Architecture Decision Records.
- Review architecture-impacting changes.
- Coordinate cross-component technical consistency.

The Solution Architect may delegate detailed design activities but retains ownership of architectural coherence.

Significant architecture decisions are subject to risk-based approval.

### 3.5 Specialist Engineering Roles

Specialist Roles execute engineering work within their defined responsibilities.

The Organization maintains the official Role catalog. Projects select the Roles they need and assign project-specific Skills and Capabilities.

The initial Role catalog is defined in `roles-and-responsibilities.md`.

### 3.6 Human Governance

Human involvement is determined by risk and authority.

Humans retain approval authority for high-impact business, security, compliance, and operational decisions.

## 4. Role, Skill, Capability, and Technology Stack Model

### 4.1 Role

A Role defines a stable organizational responsibility.

Examples:

- Backend Engineer.
- Frontend Engineer.
- Mobile Engineer.
- QA Engineer.
- Security Engineer.

Roles are defined and governed by the Organization.

Projects cannot independently create, rename, or redefine official Organization Roles.

### 4.2 Skill

A Skill represents a specific technical or professional competency.

Examples:

- C#.
- Java.
- Python.
- React.
- Flutter.
- WordPress.
- PostgreSQL.
- RabbitMQ.
- Kubernetes.

Skills may be reused across multiple Roles when relevant.

### 4.3 Capability

A Capability represents the ability to perform a broader engineering activity or solve a particular class of problems.

Examples:

- REST API Development.
- Event-Driven Architecture.
- Distributed Systems Design.
- Database Optimization.
- Mobile Application Development.
- Contract Testing.
- Threat Modeling.
- CI/CD Pipeline Design.

Capabilities may consist of multiple Skills and may be assigned to different Roles according to responsibility.

### 4.4 Technology Stack

Technology Stack is declared at Project Layer.

A project may define different technologies for different applications, services, or components.

For example:

| Component | Technology Stack |
|---|---|
| Mobile App | Flutter |
| Web App | React |
| API Gateway | .NET |
| Order Service | Java |
| Notification Service | Python |
| Website | WordPress / PHP |
| Database | PostgreSQL |
| Message Broker | RabbitMQ |
| Infrastructure | Docker / Kubernetes |

AIEO must not assume that all components in one project use the same language or framework.

### 4.5 Agent Instantiation

An Agent instance is created from an approved Role.

The project assigns the Agent:

- Project context.
- Relevant Skills.
- Required Capabilities.
- Technology Stack context.
- Task scope.
- Permissions.
- Expected deliverables.
- Applicable Quality Gates.

An Agent instance may hold multiple approved Skills and Capabilities.

One Agent instance may perform more than one Role in small projects when explicitly permitted. However, Role responsibilities and review criteria remain distinct.

## 5. Project Architecture and System Context

Projects must describe their architecture at a level appropriate to their complexity.

### 5.1 Architecture Classification

The Solution Architect identifies the architecture style and relevant boundaries, which may include:

- Monolithic.
- Modular monolith.
- Microservices.
- Distributed systems.
- Event-driven.
- Serverless.
- Hybrid architectures.

AIEO does not mandate a particular architecture style.

### 5.2 System-Level Architecture Artifacts

For projects involving multiple applications, services, or independently deployed components, the following artifacts should be maintained as applicable:

| Artifact | Purpose |
|---|---|
| System Context Diagram | Defines system boundaries and external actors/systems |
| Component Diagram | Describes applications, services, and major components |
| Service Catalog | Defines each service's responsibility and ownership |
| Dependency Map | Identifies dependencies and communication relationships |
| API / Event Contracts | Defines communication contracts |
| Data Ownership Map | Identifies authoritative data ownership |
| Architecture Decision Records | Captures significant technical decisions |
| Deployment Architecture | Describes deployment topology |
| NFR Specification | Defines performance, availability, scalability, and reliability needs |
| Security Architecture | Describes trust boundaries and security controls |

The Solution Architect owns the architectural consistency of these artifacts.

### 5.3 Component Ownership

Every major application, service, or component must have a clear functional responsibility.

The project must identify:

- What the component owns.
- What it does not own.
- Which data it is authoritative for.
- Which components it depends on.
- Which interfaces it exposes.
- Which interfaces it consumes.

### 5.4 Integration Contracts

Components that communicate must have agreed contracts.

Contracts may include:

- REST or GraphQL API specifications.
- Message/event schemas.
- Webhook specifications.
- Data exchange formats.
- Authentication and authorization requirements.
- Error handling and retry behavior.
- Compatibility and versioning rules.

Contract changes must be assessed for backward compatibility and impact on dependent components.

### 5.5 Data Ownership

Projects must avoid ambiguous ownership of business data.

The authoritative owner of each important data domain must be identified.

Cross-service data synchronization, eventual consistency, transaction boundaries, and failure recovery must be considered where relevant.

## 6. Project Lifecycle

### 6.1 Project Initiation

The project owner defines business objectives and initial scope.

Engineering Manager coordinates project setup.

Required initial outputs may include:

- Project charter or overview.
- Initial requirements.
- Stakeholder information.
- Initial constraints.
- Project configuration.
- Selected AIEO version.

### 6.2 Requirements Analysis

Product Manager analyzes and structures requirements.

Outputs include:

- Functional requirements.
- Non-functional requirements.
- User journeys.
- Acceptance criteria.
- Initial backlog.
- Business priorities.

### 6.3 Solution Architecture and Design

Solution Architect defines the technical solution.

Outputs depend on project complexity and may include:

- Architecture diagrams.
- Application and service boundaries.
- Technology Stack decisions.
- Integration contracts.
- Data ownership.
- Security architecture.
- Architecture Decision Records.

### 6.4 Implementation Planning

Engineering Manager coordinates task decomposition and execution planning.

Tasks must identify:

- Objective.
- Scope.
- Dependencies.
- Responsible Role.
- Required Skills and Capabilities.
- Technology context.
- Expected deliverables.
- Acceptance criteria.
- Quality Gates.

### 6.5 Development and Implementation

Engineering Agents execute assigned tasks.

Parallel execution is allowed when dependencies and interfaces are sufficiently defined.

For cross-component work, relevant contracts and ownership must be established before parallel implementation.

### 6.6 QA and Review

Quality validation includes applicable levels:

- Unit testing.
- Component testing.
- API and contract testing.
- Integration testing.
- End-to-end testing.
- Performance testing.
- Security testing.
- Regression testing.

Every code change must pass required automated checks.

Code Review and Security Review are distinct responsibilities. Review depth is determined by risk.

### 6.7 Release and Deployment

DevOps Engineer coordinates deployment activities.

Release must satisfy applicable Quality Gates and approval requirements.

High-risk production changes require human approval.

### 6.8 Maintenance and Continuous Improvement

The team monitors system behavior, resolves defects, addresses technical debt, and improves engineering practices.

Lessons learned may be proposed for inclusion in reusable Organization capabilities.

## 7. Work Management and Delegation

### 7.1 Work Intake

Work may originate from:

- Product backlog.
- Defects.
- Technical debt.
- Security findings.
- Operational incidents.
- Architecture improvements.
- Compliance requirements.

### 7.2 Prioritization Ownership

- Product Manager owns business priority.
- Engineering Manager owns execution priority, sequencing, and dependencies.
- Solution Architect owns technical design decisions.
- Human Project Owner resolves business conflicts and approves decisions requiring human authority.

### 7.3 Task Decomposition

Engineering Manager decomposes backlog items into executable tasks.

Tasks should be sufficiently independent to allow parallel execution without creating unnecessary integration risk.

### 7.4 Role Assignment

Engineering Manager selects from Organization-approved Roles.

The project provides the required Skills, Capabilities, and Technology Stack context.

If a required Role does not exist, the Engineering Manager must raise a proposal to Organization governance rather than inventing a new official Role.

### 7.5 Parallel Execution

Parallel execution is encouraged when:

- Task boundaries are clear.
- Dependencies are understood.
- Integration contracts are available.
- Shared resources and files are managed safely.
- Conflicting changes are controlled.

### 7.6 Task Completion

A task is complete only when:

- Required deliverables exist.
- Acceptance criteria are met.
- Required automated checks pass.
- Required reviews are complete.
- Documentation is updated where applicable.
- Dependencies and follow-up work are recorded.

## 8. Agent Collaboration and Communication

Agents collaborate through explicit task assignments and shared project artifacts.

The Engineering Manager coordinates work and resolves execution conflicts.

The Solution Architect coordinates architecture-related collaboration.

Product Manager clarifies business requirements.

Specialist Agents communicate relevant technical findings and escalate conflicts.

Agents must not silently make decisions that change another component's contract, ownership, or behavior without appropriate coordination.

## 9. Quality Management

### 9.1 Automated Quality Checks

Every code change must pass the project's required automated checks.

Examples:

- Build and compilation.
- Unit tests.
- Static analysis.
- Linting and formatting.
- Dependency vulnerability checks.
- Secret scanning.
- Contract tests.
- Integration tests.

The exact checks depend on project technology and risk.

### 9.2 Code Review

Code Reviewer assesses:

- Correctness.
- Maintainability.
- Readability.
- Design consistency.
- Error handling.
- Test quality.
- Potential regressions.

Review requirements are risk-based.

### 9.3 Security Review

Security Engineer assesses:

- Threats and attack surfaces.
- Authentication and authorization.
- Sensitive data handling.
- Dependency and supply-chain risks.
- Security configuration.
- Security architecture.
- Relevant security testing.

### 9.4 Quality Assurance

QA Engineer validates requirements and behavior at component and system levels.

Distributed projects should include contract, integration, and end-to-end testing where applicable.

## 10. Risk Management and Escalation

Agents must escalate when:

- Requirements are ambiguous or conflicting.
- A task exceeds the assigned Role's authority.
- A proposed change affects system boundaries or contracts.
- Security, privacy, compliance, or operational risks are identified.
- Required permissions are unavailable.
- Quality Gates cannot be satisfied.
- A decision has significant business impact.

Human approval is risk-based and must be traceable.

## 11. Multi-Project Operations

Each project has its own Project Layer and Runtime Layer.

Projects may reuse the same Organization Roles, Skills, Capabilities, and workflows.

Project contexts and source code remain isolated by default.

Separate project sessions and working directories must be used to prevent accidental cross-project changes.

The Organization Layer does not automatically grant an Agent access to other projects.

## 12. Operating with Claude Code

Claude Code is an execution environment for AIEO Agents.

AIEO defines reusable Role instructions, Skills, workflows, and project context.

The project must explicitly configure the applicable AIEO version and project-specific context.

Organization capabilities must be distributed through an explicit mechanism such as templates, synchronization, or a versioned plugin.

A project must not rely on implicit inheritance of files or configuration from another repository.

## 13. Organization Versioning and Project Adoption

Organization releases are versioned.

Each project records its selected AIEO version.

New projects default to the latest approved stable release.

Existing projects remain on their pinned version unless they voluntarily upgrade or a mandatory risk review requires action.

Upgrade assessments must consider:

- Compatibility.
- Breaking changes.
- Updated Role definitions.
- Updated Skills and Capabilities.
- Workflow changes.
- Migration effort.
- Security and operational impact.

## 14. Continuous Improvement

Project feedback may identify opportunities to improve:

- Roles and responsibilities.
- Skills and Capabilities.
- Agent instructions.
- Workflows.
- Quality Gates.
- Engineering standards.

Proposals are reviewed by Organization governance before becoming reusable Organization capabilities.

Project-specific workarounds must not silently become Organization standards.

---

**End of Document**