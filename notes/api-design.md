# API Design Notes

Some things I keep coming back to when designing APIs.

- **Idempotency**: Always allow retries with the same request key. Use `Idempotency-Key` headers.
- **Versioning**: URL versioning (`/v1/`) is simplest; don't overthink it.
- **Errors**: Use structured error bodies with a stable error code and a human-readable message.
- **Pagination**: Cursor-based is usually better than offset for large datasets.
- **Rate limiting**: Return `X-RateLimit-Limit` and `X-RateLimit-Remaining` headers.
- **Documentation**: Keep OpenAPI spec in sync as part of CI.

More to add as I keep tinkering.