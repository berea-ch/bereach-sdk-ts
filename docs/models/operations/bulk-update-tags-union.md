# BulkUpdateTagsUnion

Tag operations: { add, remove } or { set }


## Supported Types

### `operations.BulkUpdateTags1`

```typescript
const value: operations.BulkUpdateTags1 = {
  add: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

### `operations.BulkUpdateTags2`

```typescript
const value: operations.BulkUpdateTags2 = {
  remove: [
    "<value 1>",
  ],
};
```

### `operations.BulkUpdateTags3`

```typescript
const value: operations.BulkUpdateTags3 = {
  set: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

