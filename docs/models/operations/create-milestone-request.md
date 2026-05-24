# CreateMilestoneRequest

## Example Usage

```typescript
import { CreateMilestoneRequest } from "@clientcasa/sdk/models/operations";

let value: CreateMilestoneRequest = {
  idempotencyKey: "create-client-2026-05-24-a1b2c3",
  body: {
    parentType: "projects",
    parentId: "550e8400-e29b-41d4-a716-446655440000",
    title: "<value>",
    date: new Date("2024-09-07"),
    assigneeId: "550e8400-e29b-41d4-a716-446655440000",
    catalogItemId: "550e8400-e29b-41d4-a716-446655440000",
  },
};
```

## Fields

| Field                                                                                                                                                                                                       | Type                                                                                                                                                                                                        | Required                                                                                                                                                                                                    | Description                                                                                                                                                                                                 | Example                                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                                                                                                            | *string*                                                                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                                                          | Optional unique key that makes this create safely retryable. Replaying the same key returns the original response instead of creating a duplicate; reusing a key with a different request body returns 409. | create-client-2026-05-24-a1b2c3                                                                                                                                                                             |
| `body`                                                                                                                                                                                                      | [models.MilestoneCreate](../../models/milestone-create.md)                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                          | N/A                                                                                                                                                                                                         |                                                                                                                                                                                                             |