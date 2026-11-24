# TodoDoRuleUnion


## Supported Types

### `models.TodoDoRuleNone`

```typescript
const value: models.TodoDoRuleNone = {
  kind: "none",
};
```

### `models.TodoDoRuleFixed`

```typescript
const value: models.TodoDoRuleFixed = {
  kind: "fixed",
  day: "<value>",
};
```

### `models.TodoDoRuleEventRelative`

```typescript
const value: models.TodoDoRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 541823,
};
```

