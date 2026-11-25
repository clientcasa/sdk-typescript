# DeadlineRuleUnion3


## Supported Types

### `operations.DeadlineRuleNone3`

```typescript
const value: operations.DeadlineRuleNone3 = {
  kind: "none",
};
```

### `operations.DeadlineRuleFixed3`

```typescript
const value: operations.DeadlineRuleFixed3 = {
  kind: "fixed",
  day: "<value>",
};
```

### `operations.DeadlineRuleEventRelative3`

```typescript
const value: operations.DeadlineRuleEventRelative3 = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 562586,
};
```

