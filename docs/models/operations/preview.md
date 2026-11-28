# Preview

## Example Usage

```typescript
import { Preview } from "@clientcasa/sdk/models/operations";

let value: Preview = {
  ids: [
    "550e8400-e29b-41d4-a716-446655440000",
  ],
  impacts: [
    {
      direction: "revenue",
      currency: "Vatu",
      basis: "cash",
      period: "<value>",
      amountCents: 218997,
    },
  ],
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ids`                                                    | *string*[]                                               | :heavy_check_mark:                                       | N/A                                                      |
| `impacts`                                                | [operations.Impact](../../models/operations/impact.md)[] | :heavy_check_mark:                                       | N/A                                                      |