# DeadlineRuleUnion2


## Supported Types

### `operations.DeadlineRuleNone2`

```typescript
const value: operations.DeadlineRuleNone2 = {
  kind: "none",
};
```

### `operations.DeadlineRuleFixed2`

```typescript
const value: operations.DeadlineRuleFixed2 = {
  kind: "fixed",
  day: "<value>",
};
```

### `operations.DeadlineRuleEventRelative2`

```typescript
const value: operations.DeadlineRuleEventRelative2 = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 615302,
};
```

