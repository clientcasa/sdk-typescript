# TodoUpdateDeadlineRuleUnion


## Supported Types

### `models.TodoUpdateDeadlineRuleNone`

```typescript
const value: models.TodoUpdateDeadlineRuleNone = {
  kind: "none",
};
```

### `models.TodoUpdateDeadlineRuleFixed`

```typescript
const value: models.TodoUpdateDeadlineRuleFixed = {
  kind: "fixed",
  day: "<value>",
};
```

### `models.TodoUpdateDeadlineRuleEventRelative`

```typescript
const value: models.TodoUpdateDeadlineRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 522484,
};
```

