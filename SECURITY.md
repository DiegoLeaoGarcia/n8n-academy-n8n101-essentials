# Security Policy

## Public workflow exports

This repository stores sanitized n8n workflow exports only.

Do not commit:

- API keys or access tokens
- Real Assessment IDs
- Credential IDs or credential objects
- Private webhook URLs
- Workflow or instance IDs
- Personal or customer data
- Local environment files

## Local configuration

After importing a workflow, create or select your own n8n credentials locally and replace documented placeholders. Never push the personalized export back to this public repository.

## Reporting a security issue

If you identify exposed private data, do not open a public issue. Contact the repository owner privately and rotate any affected credential immediately.
