# Reference Implementation API

This folder describes the minimum API flow needed to try the organization-control ideas from the paper with the public reference implementation.

The API is not the paper's core contribution. The paper argues for portable organization semantics: employee identity, role authority, doctrine, work state, messages, verification, no-action, closure, replay, and governed adaptation. The API gives readers a concrete way to experiment with those ideas.

## Setup Flow

1. Sign up with an email and password.
2. Confirm the email verification code.
3. Log in to receive an access token and refresh token.
4. List your user API keys with the access token.
5. Create an organization.
6. Configure an MCP client with the API key.
7. Pass `organization_id` to org-scoped user tools when the MCP client asks which organization to operate on.

Account confirmation creates a user API key, but signup and login do not return the key value. After login, list your API keys and use one of them for MCP or API-key-authenticated calls. Create a new key only if your account has no usable key or you want an additional key.

User API keys identify the user, not a single default organization. In user-authenticated MCP sessions, organization-scoped tools require the returned `<organization_id>` as a tool argument. Employee-scoped sessions can be bound to an employee's organization, but that is outside this minimal public setup path.

## Quick Start

Use `api/quickstart.md` for the concrete request examples.

The setup path uses reader-supplied values:

- `<email>`
- `<password>`
- `<verification_code>`
- `<access_token>`
- `<api_key>`
- `<organization_id>`
- `<openai_key>`
- `<anthropic_key>`

Do not put real provider keys, account data, or private operational details in shared examples.

## What This API Is For

Use the reference implementation to try:

- creating an organization boundary;
- creating role-bound workers through the product UI or public setup flow;
- connecting an MCP-capable client to an organization-aware tool surface;
- experimenting with work records, messages, playbooks, verifier decisions, and replay concepts outside the paper's private empirical setting.

The API demonstrates reference implementation semantics; it is not empirical evidence for the paper's field-study counts.

## What This API Is Not

This is not a trading API, benchmark harness, or reproduction package for private operational records. The public package omits market names, account details, order details, strategy thresholds, raw evidence, and private implementation internals.
