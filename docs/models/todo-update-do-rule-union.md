# TodoUpdateDoRuleUnion


## Supported Types

### `models.TodoUpdateDoRuleNone`

```typescript
const value: models.TodoUpdateDoRuleNone = {
  kind: "none",
};
```

### `models.TodoUpdateDoRuleFixed`

```typescript
const value: models.TodoUpdateDoRuleFixed = {
  kind: "fixed",
  day: "<value>",
};
```

### `models.TodoUpdateDoRuleEventRelative`

```typescript
const value: models.TodoUpdateDoRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "cc736a2b-17b6-4552-81da-d2bdbd106e49",
  },
  offsetDays: 637998,
};
```

