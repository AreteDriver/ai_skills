---
name: API Design
category: architecture
priority: 3
description: Guidelines for designing clean, consistent APIs.
---

# API Design Skill

## REST Conventions
- Nouns for resources (`/users`), not verbs (`/getUsers`).
- HTTP methods convey action: GET (read), POST (create), PUT (replace), PATCH (update), DELETE (remove).
- Plural resource names: `/users/123`, not `/user/123`.
- Nest for relationships: `/users/123/orders`.
- Use query params for filtering, sorting, pagination: `?status=active&sort=-created_at&limit=20`.

## Response Design
- Consistent envelope: `{ "data": ..., "error": ..., "meta": ... }` or plain resource.
- Pick one pattern and stick with it across the entire API.
- HTTP status codes must match semantics (don't return 200 with an error body).
- Include pagination metadata: `total`, `page`, `per_page`, `next_cursor`.

## Error Responses
```json
{
  "error": {
    "code": "VALIDATION_FAILED",
    "message": "Human-readable description",
    "details": [{"field": "email", "issue": "invalid format"}]
  }
}
```

## Versioning
- URL prefix (`/v1/`) for breaking changes.
- Avoid breaking changes: add fields, don't remove or rename.

## Documentation
- Every endpoint: method, path, params, request body, response, error codes.
- Include realistic examples, not lorem ipsum.
