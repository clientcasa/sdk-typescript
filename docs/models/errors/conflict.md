# Conflict

Review the latest preview, or follow the refusal message for a billed item or closed period.


## Supported Types

### `errors.ResponseBodyError`

```typescript
const value: errors.ResponseBodyError = {
  error: {
    code: "conflict",
    message: "<value>",
    requestId: "<id>",
    details: {
      code: "transaction_delete_preview_required",
      preview: {
        ids: [
          "550e8400-e29b-41d4-a716-446655440000",
        ],
        impacts: [],
      },
      acknowledgement: "<value>",
    },
  },
};
```

### `errors.ApiError`

```typescript
const value: errors.ApiError = {
  error: {
    code: "service_unavailable",
    message: "<value>",
    requestId: "<id>",
  },
};
```

