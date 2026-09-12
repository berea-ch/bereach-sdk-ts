# ScheduledMessageCreateFirstDmUnion

Where this person's first message stands, from the one projection every surface reads. Present on list rows.


## Supported Types

### `operations.ScheduledMessageCreateFirstDmNone`

```typescript
const value: operations.ScheduledMessageCreateFirstDmNone = {
  kind: "none",
};
```

### `operations.ScheduledMessageCreateFirstDmWritten`

```typescript
const value: operations.ScheduledMessageCreateFirstDmWritten = {
  kind: "written",
  scheduledMessageId: "<id>",
};
```

### `operations.ScheduledMessageCreateFirstDmHeld`

```typescript
const value: operations.ScheduledMessageCreateFirstDmHeld = {
  kind: "held",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

### `operations.ScheduledMessageCreateFirstDmQueued`

```typescript
const value: operations.ScheduledMessageCreateFirstDmQueued = {
  kind: "queued",
  scheduledMessageId: "<id>",
  why: {
    status: "window",
    detail: "<value>",
    position: null,
    opensAt: "<value>",
    clearsItself: false,
    fixUrl: "https://shy-sermon.biz/",
  },
};
```

### `operations.ScheduledMessageCreateFirstDmSending`

```typescript
const value: operations.ScheduledMessageCreateFirstDmSending = {
  kind: "sending",
  scheduledMessageId: "<id>",
};
```

### `operations.ScheduledMessageCreateFirstDmSent`

```typescript
const value: operations.ScheduledMessageCreateFirstDmSent = {
  kind: "sent",
  scheduledMessageId: "<id>",
  sentAt: "<value>",
};
```

### `operations.ScheduledMessageCreateFirstDmFailed`

```typescript
const value: operations.ScheduledMessageCreateFirstDmFailed = {
  kind: "failed",
  scheduledMessageId: "<id>",
  reason: "<value>",
  canRequeue: true,
};
```

### `operations.ScheduledMessageCreateFirstDmCancelled`

```typescript
const value: operations.ScheduledMessageCreateFirstDmCancelled = {
  kind: "cancelled",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

