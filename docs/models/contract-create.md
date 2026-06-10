# ContractCreate

## Example Usage

```typescript
import { ContractCreate } from "@clientcasa/sdk/models";

let value: ContractCreate = {
  title: "<value>",
  clientId: "550e8400-e29b-41d4-a716-446655440000",
  billingContactId: "550e8400-e29b-41d4-a716-446655440000",
  projectId: "550e8400-e29b-41d4-a716-446655440000",
  sourceTemplateId: "550e8400-e29b-41d4-a716-446655440000",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          | Example                              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `title`                              | *string*                             | :heavy_check_mark:                   | N/A                                  |                                      |
| `clientId`                           | *string*                             | :heavy_check_mark:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `billingContactId`                   | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `projectId`                          | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `sourceTemplateId`                   | *string*                             | :heavy_minus_sign:                   | UUID v4                              | 550e8400-e29b-41d4-a716-446655440000 |
| `issueDate`                          | [Date](../types/rfcdate.md)          | :heavy_minus_sign:                   | N/A                                  |                                      |
| `effectiveDate`                      | [Date](../types/rfcdate.md)          | :heavy_minus_sign:                   | N/A                                  |                                      |
| `expirationDate`                     | [Date](../types/rfcdate.md)          | :heavy_minus_sign:                   | N/A                                  |                                      |
| `contractValue`                      | *number*                             | :heavy_minus_sign:                   | N/A                                  |                                      |