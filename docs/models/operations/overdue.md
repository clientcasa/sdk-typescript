# Overdue

Filter by the derived overdue condition. `true` → sent/partial invoices past their due date; `false` → everything else. (Replaces the removed `status=overdue` filter.)

## Example Usage

```typescript
import { Overdue } from "@clientcasa/sdk/models/operations";

let value: Overdue = "false";
```

## Values

```typescript
"true" | "false"
```