# State

## Example Usage

```typescript
import { State } from "@clientcasa/sdk/models";

let value: State = "ready";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"ready" | "updating" | "review" | "unavailable" | Unrecognized<string>
```