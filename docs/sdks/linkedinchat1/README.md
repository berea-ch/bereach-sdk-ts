# LinkedinChat

## Overview

### Available Operations

* [listInboxConversations](#listinboxconversations) - List LinkedIn inbox conversations
* [getMessages](#getmessages) - Read messages from a conversation
* [markAllRead](#markallread) - Mark all conversations as read
* [listArchived](#listarchived) - List archived conversations
* [react](#react) - React to a message with emoji
* [sendTypingIndicator](#sendtypingindicator) - Send typing indicator
* [getUnreadCount](#getunreadcount) - Get unread message count

## listInboxConversations

List inbox conversations for the authenticated user. Returns conversations with participants, last message, and read status. Paginate via nextCursor.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listInboxConversations" method="post" path="/chats/linkedin" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.listInboxConversations({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatListInboxConversations } from "bereach/funcs/linkedin-chat-list-inbox-conversations.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatListInboxConversations(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatListInboxConversations failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListInboxConversationsRequest](../../models/operations/list-inbox-conversations-request.md)                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListInboxConversationsResponse](../../models/operations/list-inbox-conversations-response.md)\>**

### Errors

| Error Type                                            | Status Code                                           | Content Type                                          |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| errors.ListInboxConversationsBadRequestError          | 400                                                   | application/json                                      |
| errors.ListInboxConversationsUnauthorizedError        | 401                                                   | application/json                                      |
| errors.ListInboxConversationsForbiddenError           | 403                                                   | application/json                                      |
| errors.ListInboxConversationsNotFoundError            | 404                                                   | application/json                                      |
| errors.ListInboxConversationsConflictError            | 409                                                   | application/json                                      |
| errors.ListInboxConversationsGoneError                | 410                                                   | application/json                                      |
| errors.ListInboxConversationsUnprocessableEntityError | 422                                                   | application/json                                      |
| errors.ListInboxConversationsTooManyRequestsError     | 429                                                   | application/json                                      |
| errors.ListInboxConversationsInternalServerError      | 500                                                   | application/json                                      |
| errors.BereachDefaultError                            | 4XX, 5XX                                              | \*/\*                                                 |

## getMessages

Fetch messages from a specific LinkedIn conversation. 0 credits.

Pass the full `conversationUrn` as returned by `/chats/linkedin` or `/chats/linkedin/search`. No parsing required — the server handles extraction internally.

Example: `{ "conversationUrn": "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)" }`

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getConversationMessages" method="post" path="/chats/linkedin/messages" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.getMessages({
    conversationUrn: "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUxZGQ3MTMt...XzEwMA==)",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatGetMessages } from "bereach/funcs/linkedin-chat-get-messages.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatGetMessages(bereach, {
    conversationUrn: "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUxZGQ3MTMt...XzEwMA==)",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatGetMessages failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetConversationMessagesRequest](../../models/operations/get-conversation-messages-request.md)                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetConversationMessagesResponse](../../models/operations/get-conversation-messages-response.md)\>**

### Errors

| Error Type                                             | Status Code                                            | Content Type                                           |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| errors.GetConversationMessagesBadRequestError          | 400                                                    | application/json                                       |
| errors.GetConversationMessagesUnauthorizedError        | 401                                                    | application/json                                       |
| errors.GetConversationMessagesForbiddenError           | 403                                                    | application/json                                       |
| errors.GetConversationMessagesNotFoundError            | 404                                                    | application/json                                       |
| errors.GetConversationMessagesConflictError            | 409                                                    | application/json                                       |
| errors.GetConversationMessagesGoneError                | 410                                                    | application/json                                       |
| errors.GetConversationMessagesUnprocessableEntityError | 422                                                    | application/json                                       |
| errors.GetConversationMessagesTooManyRequestsError     | 429                                                    | application/json                                       |
| errors.GetConversationMessagesInternalServerError      | 500                                                    | application/json                                       |
| errors.BereachDefaultError                             | 4XX, 5XX                                               | \*/\*                                                  |

## markAllRead

Mark all LinkedIn inbox conversations as read. 0 credits.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="markAllConversationsRead" method="post" path="/chats/linkedin/mark-all-read" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.markAllRead({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatMarkAllRead } from "bereach/funcs/linkedin-chat-mark-all-read.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatMarkAllRead(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatMarkAllRead failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.MarkAllConversationsReadRequest](../../models/operations/mark-all-conversations-read-request.md)                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.MarkAllConversationsReadResponse](../../models/operations/mark-all-conversations-read-response.md)\>**

### Errors

| Error Type                                              | Status Code                                             | Content Type                                            |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| errors.MarkAllConversationsReadBadRequestError          | 400                                                     | application/json                                        |
| errors.MarkAllConversationsReadUnauthorizedError        | 401                                                     | application/json                                        |
| errors.MarkAllConversationsReadForbiddenError           | 403                                                     | application/json                                        |
| errors.MarkAllConversationsReadNotFoundError            | 404                                                     | application/json                                        |
| errors.MarkAllConversationsReadConflictError            | 409                                                     | application/json                                        |
| errors.MarkAllConversationsReadGoneError                | 410                                                     | application/json                                        |
| errors.MarkAllConversationsReadUnprocessableEntityError | 422                                                     | application/json                                        |
| errors.MarkAllConversationsReadTooManyRequestsError     | 429                                                     | application/json                                        |
| errors.MarkAllConversationsReadInternalServerError      | 500                                                     | application/json                                        |
| errors.BereachDefaultError                              | 4XX, 5XX                                                | \*/\*                                                   |

## listArchived

List archived LinkedIn conversations. 0 credits.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listArchivedConversations" method="post" path="/chats/linkedin/archived" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.listArchived({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatListArchived } from "bereach/funcs/linkedin-chat-list-archived.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatListArchived(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatListArchived failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListArchivedConversationsRequest](../../models/operations/list-archived-conversations-request.md)                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListArchivedConversationsResponse](../../models/operations/list-archived-conversations-response.md)\>**

### Errors

| Error Type                                               | Status Code                                              | Content Type                                             |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| errors.ListArchivedConversationsBadRequestError          | 400                                                      | application/json                                         |
| errors.ListArchivedConversationsUnauthorizedError        | 401                                                      | application/json                                         |
| errors.ListArchivedConversationsForbiddenError           | 403                                                      | application/json                                         |
| errors.ListArchivedConversationsNotFoundError            | 404                                                      | application/json                                         |
| errors.ListArchivedConversationsConflictError            | 409                                                      | application/json                                         |
| errors.ListArchivedConversationsGoneError                | 410                                                      | application/json                                         |
| errors.ListArchivedConversationsUnprocessableEntityError | 422                                                      | application/json                                         |
| errors.ListArchivedConversationsTooManyRequestsError     | 429                                                      | application/json                                         |
| errors.ListArchivedConversationsInternalServerError      | 500                                                      | application/json                                         |
| errors.BereachDefaultError                               | 4XX, 5XX                                                 | \*/\*                                                    |

## react

Add an emoji reaction to a LinkedIn message. 0 credits.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="reactToMessage" method="post" path="/chats/linkedin/react" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.react({
    messageUrn: "urn:li:msg_message:(urn:li:fsd_profile:ACoAAXXX,2-MTcw...)",
    emoji: "👍",
    conversationUrn: "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatReact } from "bereach/funcs/linkedin-chat-react.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatReact(bereach, {
    messageUrn: "urn:li:msg_message:(urn:li:fsd_profile:ACoAAXXX,2-MTcw...)",
    emoji: "👍",
    conversationUrn: "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatReact failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ReactToMessageRequest](../../models/operations/react-to-message-request.md)                                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ReactToMessageResponse](../../models/operations/react-to-message-response.md)\>**

### Errors

| Error Type                                    | Status Code                                   | Content Type                                  |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| errors.ReactToMessageBadRequestError          | 400                                           | application/json                              |
| errors.ReactToMessageUnauthorizedError        | 401                                           | application/json                              |
| errors.ReactToMessageForbiddenError           | 403                                           | application/json                              |
| errors.ReactToMessageNotFoundError            | 404                                           | application/json                              |
| errors.ReactToMessageConflictError            | 409                                           | application/json                              |
| errors.ReactToMessageGoneError                | 410                                           | application/json                              |
| errors.ReactToMessageUnprocessableEntityError | 422                                           | application/json                              |
| errors.ReactToMessageTooManyRequestsError     | 429                                           | application/json                              |
| errors.ReactToMessageInternalServerError      | 500                                           | application/json                              |
| errors.BereachDefaultError                    | 4XX, 5XX                                      | \*/\*                                         |

## sendTypingIndicator

Send a typing indicator to a LinkedIn conversation, simulating natural typing behavior. 0 credits.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="sendTypingIndicator" method="post" path="/chats/linkedin/typing" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.sendTypingIndicator({
    conversationUrn: "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatSendTypingIndicator } from "bereach/funcs/linkedin-chat-send-typing-indicator.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatSendTypingIndicator(bereach, {
    conversationUrn: "urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatSendTypingIndicator failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SendTypingIndicatorRequest](../../models/operations/send-typing-indicator-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SendTypingIndicatorResponse](../../models/operations/send-typing-indicator-response.md)\>**

### Errors

| Error Type                                         | Status Code                                        | Content Type                                       |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| errors.SendTypingIndicatorBadRequestError          | 400                                                | application/json                                   |
| errors.SendTypingIndicatorUnauthorizedError        | 401                                                | application/json                                   |
| errors.SendTypingIndicatorForbiddenError           | 403                                                | application/json                                   |
| errors.SendTypingIndicatorNotFoundError            | 404                                                | application/json                                   |
| errors.SendTypingIndicatorConflictError            | 409                                                | application/json                                   |
| errors.SendTypingIndicatorGoneError                | 410                                                | application/json                                   |
| errors.SendTypingIndicatorUnprocessableEntityError | 422                                                | application/json                                   |
| errors.SendTypingIndicatorTooManyRequestsError     | 429                                                | application/json                                   |
| errors.SendTypingIndicatorInternalServerError      | 500                                                | application/json                                   |
| errors.BereachDefaultError                         | 4XX, 5XX                                           | \*/\*                                              |

## getUnreadCount

Get the number of unread LinkedIn messages/conversations. 0 credits.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getUnreadCount" method="post" path="/chats/linkedin/unread" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinChat.getUnreadCount({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinChatGetUnreadCount } from "bereach/funcs/linkedin-chat-get-unread-count.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinChatGetUnreadCount(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinChatGetUnreadCount failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetUnreadCountRequest](../../models/operations/get-unread-count-request.md)                                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetUnreadCountResponse](../../models/operations/get-unread-count-response.md)\>**

### Errors

| Error Type                                    | Status Code                                   | Content Type                                  |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| errors.GetUnreadCountBadRequestError          | 400                                           | application/json                              |
| errors.GetUnreadCountUnauthorizedError        | 401                                           | application/json                              |
| errors.GetUnreadCountForbiddenError           | 403                                           | application/json                              |
| errors.GetUnreadCountNotFoundError            | 404                                           | application/json                              |
| errors.GetUnreadCountConflictError            | 409                                           | application/json                              |
| errors.GetUnreadCountGoneError                | 410                                           | application/json                              |
| errors.GetUnreadCountUnprocessableEntityError | 422                                           | application/json                              |
| errors.GetUnreadCountTooManyRequestsError     | 429                                           | application/json                              |
| errors.GetUnreadCountInternalServerError      | 500                                           | application/json                              |
| errors.BereachDefaultError                    | 4XX, 5XX                                      | \*/\*                                         |