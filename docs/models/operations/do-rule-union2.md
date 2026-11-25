# DoRuleUnion2


## Supported Types

### `operations.DoRuleNone2`

```typescript
const value: operations.DoRuleNone2 = {
  kind: "none",
};
```

### `operations.DoRuleFixed2`

```typescript
const value: operations.DoRuleFixed2 = {
  kind: "fixed",
  day: "<value>",
};
```

### `operations.DoRuleEventRelative2`

```typescript
const value: operations.DoRuleEventRelative2 = {
  kind: "event-relative",
  anchor: {
    kind: "pending",
    label: "<value>",
    setEventDateLater: true,
  },
  offsetDays: 240360,
};
```

