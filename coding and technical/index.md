# Role-Based Coding and Technical Prompts

## QA (Quality Assurance)

1. "Generate test automation code for [scenario] using [framework], including setup, assertions, cleanup, and readable test names."
2. "Write SQL queries to validate data correctness for [feature/workflow], including positive checks and anomaly detection."
3. "Create a regex to identify [pattern] in logs or test data, and explain edge cases it will and will not match."
4. "Write a shell command or script to collect QA evidence for [system], including logs, versions, and environment details."
5. "Generate API test cases for [endpoint] with request examples, expected responses, and error assertions."
6. "Debug this failing automated test [test/code] and suggest the most likely fix."
7. "Refactor this test code [code] to reduce brittleness and improve readability."
8. "Write a data seeding script for QA scenarios involving [entities/conditions]."
9. "Create a checklist of technical validations for [release], including database, API, UI, permissions, and logs."
10. "Explain this stack trace [trace] in QA terms and identify what evidence to capture next."

## Business Analysts

1. "Write SQL to extract data needed for analyzing [business process/metric], with clear column names and filters."
2. "Create a simple data dictionary for [dataset] from these field descriptions [fields]."
3. "Generate pseudo-code for the business rules in [requirement] so developers and stakeholders can verify logic."
4. "Write an example JSON payload representing [business object/workflow] with realistic sample values."
5. "Translate this process logic [logic] into decision-table format with conditions, outcomes, and exceptions."
6. "Create a Mermaid process diagram for [workflow] based on this description [description]."
7. "Write validation rules for [form/process] in business-readable language and developer-friendly pseudo-code."
8. "Generate sample test data rows for [scenario] that cover common cases and exceptions."
9. "Explain this API or integration spec [spec] in business terms, including data flow and operational impact."
10. "Create a mapping table from source fields to target fields for [migration/integration]."

## Developers

1. "Write code in [language/framework] to implement [feature], following these constraints: [constraints]."
2. "Debug this code [code/error] and explain the likely cause, minimal fix, and tests to add."
3. "Refactor this code [code] for readability, maintainability, and smaller functions without changing behavior."
4. "Generate unit tests for [function/module], including edge cases, invalid input, and expected failures."
5. "Write a SQL query for [task], optimizing for correctness first and performance second."
6. "Create a regex for [pattern], explain it step by step, and provide matching and non-matching examples."
7. "Generate a shell command or script to automate [developer task] safely and repeatably."
8. "Explain this code [code] line by line, then summarize the design and likely failure points."
9. "Design an API endpoint for [use case], including schema, validation, errors, tests, and documentation."
10. "Write migration code for [schema/data change], including rollback considerations and validation queries."

## Senior Developers

1. "Design the technical approach for [system/feature], including architecture, interfaces, data model, failure modes, and rollout."
2. "Review this code or design [code/design] for correctness, maintainability, scalability, security, and operational readiness."
3. "Refactor this module [module] using an incremental migration plan that avoids breaking existing behavior."
4. "Write an RFC-quality technical design for introducing [technology/pattern] into [system]."
5. "Debug this production issue [issue] by proposing hypotheses, instrumentation, experiments, and rollback options."
6. "Generate a migration script and validation plan for moving from [old schema/system] to [new schema/system]."
7. "Design observability for [service], including logs, metrics, traces, dashboards, alerts, and runbook checks."
8. "Create a performance optimization plan for [system], including profiling, bottleneck analysis, experiments, and safeguards."
9. "Write contract tests for [service/API] and explain how they fit into CI/CD and versioning."
10. "Explain how to make [system] more reliable under partial failure, retries, timeouts, backpressure, and dependency outages."

## Product People

1. "Explain the technical feasibility of [feature] in product terms, including complexity, dependencies, risks, and alternatives."
2. "Generate product-facing acceptance criteria for [feature] that engineering and QA can turn into implementation and tests."
3. "Translate this technical design [design] into product implications, user impact, sequencing, and trade-offs."
4. "Create a technical discovery checklist for [feature] covering data, APIs, permissions, integrations, and analytics."
5. "Write example API payloads or event schemas that express the product behavior for [workflow]."
6. "Explain this bug [bug] in terms of customer impact, scope, workaround, fix approach, and release risk."
7. "Generate analytics event definitions for [feature], including event name, trigger, properties, and intended questions."
8. "Create a product-readable migration plan for [technical change], including user impact and communication needs."
9. "Summarize developer estimates for [feature] into product planning assumptions, risks, and decision points."
10. "Write a technical FAQ for go-to-market teams about [feature/integration]."
