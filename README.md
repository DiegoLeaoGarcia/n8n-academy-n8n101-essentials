# n8n Academy N8N101 Essentials — Automation Portfolio

[![n8n](https://img.shields.io/badge/n8n-Academy_N8N101-EA4B71?logo=n8n&logoColor=white)](https://learn.n8n.io/)
![Final Exam](https://img.shields.io/badge/final_exam-16%2F16-2ea44f)
![Grade](https://img.shields.io/badge/weighted_grade-100%25-2ea44f)
![Workflow](https://img.shields.io/badge/workflow_validation-passing-0B8793)
[![Credential](https://img.shields.io/badge/n8n-verified_credential-7B68EE)](https://badges.n8n.io/ed66725c-e39f-46ab-8e2b-a95b8aa1bd88#acc.aACPdsET)

Professional portfolio documenting the practical work completed in the official **n8n Academy N8N101 Essentials** course.

The main project is a production-style sales data pipeline that retrieves authenticated data, transforms and branches item streams, filters delivered orders, calculates regional metrics, creates a CSV report, handles binary data, and sends validated results to external endpoints.

> **Educational attribution:** The course structure and assessment endpoints belong to n8n Academy. The implementation, troubleshooting record, security review, diagrams, documentation, and repository organization are my own portfolio work. n8n and the n8n logo are trademarks of n8n GmbH.

## Verified results

| Assessment | Result |
| --- | :---: |
| Section 1 hands-on workflow | ✅ 1/1 |
| Section 1 knowledge check | ✅ 5/5 |
| Section 2 data transformation workflow | ✅ 3/3 |
| Section 2 knowledge check | ✅ 5/5 |
| Final exam | ✅ 16/16 |
| Weighted grade | ✅ 100% |

**[View the public n8n credential →](https://badges.n8n.io/ed66725c-e39f-46ab-8e2b-a95b8aa1bd88#acc.aACPdsET)**

## Portfolio project

### Sales Data Pipeline

The workflow processes 50 sales orders through two parallel branches:

1. **Operational branch** — transforms every order, calculates its total, aggregates all records, and sends the processed dataset for validation.
2. **Analytics branch** — retains delivered orders, summarizes revenue and order volume by region, validates the analysis, enriches the report with metadata, generates a CSV file, and uploads the binary report.

![Sales Data Pipeline architecture](./02-data-flow-and-transformation/sales-data-pipeline/assets/workflow-architecture.svg)

**Core capabilities**

- Manual workflow triggering
- Header-authenticated HTTP requests
- Arrays and n8n item structure
- Split Out and Aggregate transformations
- Dynamic expressions with `$json` and `$now`
- Parallel workflow branches
- Conditional filtering
- Regional sum, count, and average calculations
- Field renaming and report metadata
- CSV generation and binary file upload
- Secure, sanitized public workflow exports

**[Open the complete project documentation →](./02-data-flow-and-transformation/sales-data-pipeline/)**

## Course structure

| Section | Status | Evidence |
| --- | :---: | --- |
| [01 — Getting Started](./01-getting-started/) | ✅ Completed | Authenticated first workflow |
| [02 — Data Flow & Transformation](./02-data-flow-and-transformation/sales-data-pipeline/) | ✅ Completed | Sales Data Pipeline |
| [03 — Final Exam & Wrap-up](./03-final-exam-and-wrap-up/) | ✅ Completed | 16/16 and verified credential |

## Repository structure

```text
.
├── 01-getting-started/
│   └── README.md
├── 02-data-flow-and-transformation/
│   └── sales-data-pipeline/
│       ├── assets/
│       │   └── workflow-architecture.svg
│       ├── README.md
│       └── workflow.json
├── 03-final-exam-and-wrap-up/
│   └── README.md
├── .github/workflows/
│   └── validate-workflow.yml
├── .gitignore
├── LICENSE
├── SECURITY.md
└── README.md
```

## Importing the workflow

1. Download [`workflow.json`](./02-data-flow-and-transformation/sales-data-pipeline/workflow.json).
2. In n8n, choose **Import from File**.
3. Create or select your own **Header Auth** credential.
4. Replace every `YOUR_ASSESSMENT_ID` placeholder with your own assessment ID.
5. Confirm that `ConvertToCSV` writes the binary file to `report`.
6. Confirm that `SendReport` reads the binary field `report`.
7. Review every node before executing or publishing the workflow.

## Security and privacy

The public export contains no API keys, credential IDs, personal assessment IDs, workflow IDs, instance IDs, or private URLs. Credentials must be configured locally after import.

GitHub Actions validates workflow JSON structure and blocks common private metadata patterns on every push and pull request.

## Skills demonstrated

- Workflow orchestration
- REST API integration
- Header authentication
- JSON and array navigation
- Item linking and expressions
- Branching and filtering
- Data transformation and aggregation
- File generation
- Binary data handling
- Debugging HTTP 422/503 and binary-field errors
- Secure GitHub documentation

## Author

**Diego Rafael Leao Garcia**  
Automation and AI Engineering student focused on n8n, Python, APIs, databases, Docker, and applied artificial intelligence.

## Disclaimer

This is an independent educational portfolio and is not an official n8n repository. Refer to the official n8n Academy and n8n documentation for the original training material and certification path.

## License

Released under the [MIT License](./LICENSE).
