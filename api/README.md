# Reference Implementation API

Use this guide to create a synthetic organization and try the paper's organization-control ideas in a few minutes.

MCP is the preferred path: it exposes the full 16-tool organization surface so you can list employees, message the manager, read inboxes, inspect playbooks, and try manager-authorized changes without learning every HTTP endpoint.

Safety: use non-sensitive examples. Do not paste private trading records, account data, order data, or confidential operational records into public experiments. Only enter provider keys when configuring the organization.

## What You Will Set Up

1. A user account with an automatically created user API key.
2. A synthetic organization with an automatically created manager employee.
3. Either an MCP client connection or a few direct API calls.

The API demonstrates reference implementation semantics. It is not empirical evidence for the paper's field-study counts.

Keep these values as you go: `access_token`, `api_key`, `organization_id`, `manager_employee_id`, and `message_id`.

## 1. Request Email Verification

```sh
curl -X POST "https://api.promptfunctions.com/v1/signup" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "<email>",
    "password": "<password>"
  }'
```

## 2. Confirm Signup

Use the verification code from your email.

```sh
curl -X POST "https://api.promptfunctions.com/v1/signup" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "<email>",
    "verification_code": "<verification_code>",
    "name": "Your Name"
  }'
```

## 3. Log In

```sh
curl -X POST "https://api.promptfunctions.com/v1/login" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "<email>",
    "password": "<password>"
  }'
```

Copy the returned `access_token`.

## 4. Get Your User API Key

Account confirmation creates a user API key. List your keys:

```sh
curl -X GET "https://api.promptfunctions.com/v1/api_key?limit=5" \
  -H "Authorization: Bearer <access_token>"
```

Copy one returned `api_key`. If no key is listed, create one:

```sh
curl -X POST "https://api.promptfunctions.com/v1/api_key" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -d '{}'
```

## 5. Create A Synthetic Organization

For model-backed employee responses, provide at least one model provider key. This example uses OpenAI; you can use `anthropic_key` instead or include both.

```sh
curl -X POST "https://api.promptfunctions.com/v1/organization" \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: <api_key>" \
  -d '{
    "name": "Institutional Control Lab",
    "openai_key": "<openai_key>"
  }'
```

Creating an organization automatically creates its manager employee. Copy the returned `organization_id` and `manager_employee_id`.

## 6A. Preferred: Use MCP

For MCP clients that accept JSON config, add:

```json
{
  "mcpServers": {
    "ai-institutions": {
      "url": "https://api.promptfunctions.com/mcp",
      "headers": {
        "Authorization": "Bearer <api_key>"
      }
    }
  }
}
```

Then ask your MCP client:

```text
List the available tools. Then use organization_id <organization_id> to list employees, identify the manager, ask the manager what they are responsible for and whether the organization already has playbooks or other employees, and read the manager inbox for message status. Do not use private records or sensitive data.
```

What you should see: user and manager callers can access 16 organization tools covering employees, messages, inboxes, profiles, playbooks, role edits, tool edits, hiring, termination, and playbook mutation. Regular employee callers see the six participation tools for listing, messaging, inbox/profile reads, and playbook reads.

## 6B. Alternative: Use Direct HTTP Calls

Use this path if you want to try the basic organization surface with `curl`.

List employees:

```sh
curl -X GET "https://api.promptfunctions.com/v1/employee?organization_id=<organization_id>&limit=20" \
  -H "X-Api-Key: <api_key>"
```

Message the manager:

```sh
curl -X POST "https://api.promptfunctions.com/v1/message" \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: <api_key>" \
  -d '{
    "employee_id": "<manager_employee_id>",
    "text": "Hi, I just created this organization. What are you responsible for as the manager, and do we already have any playbooks or other employees I should know about?"
  }'
```

Copy the returned `message_id`, then poll it:

```sh
curl -X GET "https://api.promptfunctions.com/v1/message?message_id=<message_id>" \
  -H "X-Api-Key: <api_key>"
```

Or read the manager inbox:

```sh
curl -X GET "https://api.promptfunctions.com/v1/message?employee_id=<manager_employee_id>&limit=10" \
  -H "X-Api-Key: <api_key>"
```

Message handling is asynchronous. If the response is not ready, wait briefly and poll again.

## Boundary

This is not a trading API, benchmark harness, or reproduction package for private operational records. The public package omits market names, account details, order details, strategy thresholds, raw evidence, and private implementation internals.
