# TodoDeadlineRuleUnion


## Supported Types

### `models.TodoDeadlineRuleNone`

```typescript
const value: models.TodoDeadlineRuleNone = {
  kind: "none",
};
```

### `models.TodoDeadlineRuleFixed`

```typescript
const value: models.TodoDeadlineRuleFixed = {
  kind: "fixed",
  day: "<value>",
};
```

### `models.TodoDeadlineRuleEventRelative`

```typescript
const value: models.TodoDeadlineRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 866946,
};
```

