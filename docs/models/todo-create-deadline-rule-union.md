# TodoCreateDeadlineRuleUnion


## Supported Types

### `models.TodoCreateDeadlineRuleNone`

```typescript
const value: models.TodoCreateDeadlineRuleNone = {
  kind: "none",
};
```

### `models.TodoCreateDeadlineRuleFixed`

```typescript
const value: models.TodoCreateDeadlineRuleFixed = {
  kind: "fixed",
  day: "<value>",
};
```

### `models.TodoCreateDeadlineRuleEventRelative`

```typescript
const value: models.TodoCreateDeadlineRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 511127,
};
```

