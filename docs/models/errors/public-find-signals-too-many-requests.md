# PublicFindSignalsTooManyRequests

Rate limit exceeded. Read retryAfter for the wait time in seconds. The body is the flat `{ error: "<text>" }` form, with `code` when the answer carries one; a few answers use the envelope.


## Supported Types

### `errors.ResponseBodyTooManyRequestsError1`

```typescript
const value: errors.ResponseBodyTooManyRequestsError1 = {
  error: "<value>",
};
```

### `errors.ResponseBodyTooManyRequestsError2`

```typescript
const value: errors.ResponseBodyTooManyRequestsError2 = {
  error: {
    code: "<value>",
    message: "<value>",
  },
};
```

