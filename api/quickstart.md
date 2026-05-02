# API Setup Notes

These examples show the minimal public setup path for trying the reference implementation. Replace angle-bracket values before running the commands.

Base URL:

```text
https://api.promptfunctions.com
```

## 1. Request Email Verification

```sh
curl -X POST "https://api.promptfunctions.com/v1/signup" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "<email>",
    "password": "<password>"
  }'
```

Expected result:

```json
{
  "message": "email verification code has been sent to <email>"
}
```

## 2. Confirm Signup

```sh
curl -X POST "https://api.promptfunctions.com/v1/signup" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "<email>",
    "verification_code": "<verification_code>",
    "name": "Your Name"
  }'
```

Expected result includes account metadata such as:

```json
{
  "user_id": "...",
  "email": "<email>",
  "credits": 2000
}
```

This response does not include a user API key.

## 3. Log In

```sh
curl -X POST "https://api.promptfunctions.com/v1/login" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "<email>",
    "password": "<password>"
  }'
```

Expected result includes:

```json
{
  "user_id": "...",
  "email": "<email>",
  "credits": 2000,
  "access_token": "<access_token>",
  "refresh_token": "<refresh_token>"
}
```

The access token is used for account setup calls such as creating an API key.

## 4. Get A User API Key

Account confirmation creates a user API key, but signup and login do not return the key value. After login, list your keys:

```sh
curl -X GET "https://api.promptfunctions.com/v1/api_key?limit=5" \
  -H "Authorization: Bearer <access_token>"
```

Expected result:

```json
{
  "result": [
    {
      "api_key": "<api_key>",
      "created_timestamp": 1760000000
    }
  ]
}
```

Create a new key only if no usable key is listed or you want an additional key:

```sh
curl -X POST "https://api.promptfunctions.com/v1/api_key" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -d '{}'
```

Expected result:

```json
{
  "api_key": "<api_key>",
  "created_timestamp": 1760000000
}
```

Use one listed or newly created API key for normal API-key-authenticated calls and for MCP authorization.

## 5. Create An Organization

```sh
curl -X POST "https://api.promptfunctions.com/v1/organization" \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: <api_key>" \
  -d '{
    "name": "Institutional Control Lab",
    "openai_key": "<openai_key>",
    "anthropic_key": "<anthropic_key>"
  }'
```

Provider keys are optional for creation, but an organization needs at least one configured model provider to run model-backed work.

Expected result:

```json
{
  "organization_id": "<organization_id>",
  "name": "Institutional Control Lab",
  "created_timestamp": 1760000000,
  "has_openai_key": true,
  "has_anthropic_key": true
}
```

## 6. Configure MCP

Use the user API key as the MCP authorization token. Most MCP clients let you configure an endpoint URL and headers.

Endpoint:

```text
https://api.promptfunctions.com/mcp
```

Headers:

```text
Authorization: Bearer <api_key>
```

Some clients also accept the raw token value without the `Bearer` prefix.

User API keys identify the user, not a single default organization. When a user-authenticated MCP tool operates on one organization, pass the returned `<organization_id>` in that tool call. For example, list or create organization-scoped employees and playbooks against the organization you created in Step 5.

## Minimal Sanity Check

After configuration, the MCP client should be able to discover the available organization tools. From there, start with a non-sensitive organization and synthetic work examples. Do not use private trading records, account data, order data, or strategy details in public experiments.
