# Overdue

Filter by the derived overdue condition. `true` → open (`sent`) invoices past their due date with a balance owing; `false` → everything else.

## Example Usage

```typescript
import { Overdue } from "@clientcasa/sdk/models/operations";

let value: Overdue = "false";
```

## Values

```typescript
"true" | "false"
```