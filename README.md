<p align="center">
    <a href="https://croct.com">
        <img src="https://cdn.croct.io/brand/logo/repo-icon-green.svg" alt="Croct" height="80"/>
    </a>
    <br />
    <strong>Export API Node Client</strong>
    <br />
    Node.js client for the Croct Export API.
</p>

<p align="center">
    <img alt="Language" src="https://img.shields.io/badge/language-Node-blue" />
    <a href="https://www.npmjs.com/package/@croct/export"><img alt="Version" src="https://img.shields.io/npm/v/@croct/export"/></a>
    <br />
    <br />
    <a href="https://github.com/croct-tech/exporter-client-node/releases">📦 Releases</a>
    ·
    <a href="https://github.com/croct-tech/exporter-client-node/issues">🐞 Report Bug</a>
    ·
    <a href="https://github.com/croct-tech/exporter-client-node/issues">✨ Request Feature</a>
</p>

## Introduction

The Export API Client for Node allows any application written in server-side JavaScript to export events, sessions,
and users with a few lines of code.

## Getting Started

The following steps will walk you through installing the client and integrating it into your application.

### Installation

The recommended way to install the library is via [NPM](https://npmjs.com).

Run the following command to add the client as a dependency to your project and then install it:

```sh
npm install @croct/export
```

### Usage

Now the library is installed, you need to initialize the client using the API key of the application you want to 
export data:

```ts
import {Configuration, ExportApi} from '@croct/export';

const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));
```

From this point, you are all set to export data using one of the [export methods](#api-reference). However, developers 
are usually interested in implementing a routine to export data periodically. If that is the case, there are two 
approaches you can take to fetch data incrementally, as you will find out in the following sections.

#### Incremental export

The following sections present different approaches for exporting data incrementally so you can choose the one that 
best suits your needs.

###### Stateful approach 

Every request to the Export API returns a cursor that you can use in subsequent requests to fetch the next 
batch of data. You can keep making calls until no data is left to export – at that point, you can store the cursor and 
resume the export later.

The following example illustrates how you can fetch data incrementally using cursors:

```ts
import {Configuration, ExportApi} from '@croct/export';

async function loadCursor(): Promise<string|undefined> {
    // Read the previous cursor from a database, file, or somewhere else
}

async function saveCursor(cursor: string): Promise<void> {
    // Write the current cursor to a database, file, or somewhere else
}

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = await loadCursor();

    // The maximum number of events per request 
    const pageSize = 100;

    // The maximum number of events to export
    let limit = 1000;

    while (limit >= pageSize) {
        const {data: {items: events, nextCursor}} = await api.exportEvents({
            pageSize: pageSize,
            cursor: cursor,
        });

        cursor = nextCursor;
        limit = events.length > 0 ? limit - events.length : 0;
    }
    
    await saveCursor(cursor);
})();
```

By reusing the previous cursor on subsequent requests, you guarantee that no data is missed between exports. However, 
it requires some extra work to store the cursor between exports so that the next export can start from where the 
previous one left off.

###### Stateless approach

If storing cursors is not an option, you can alternatively fetch data based on a time interval. For example, you can 
set up a job to daily export data from the previous day:

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    const today = new Date();
    today.setHours(0, 0, 0, 0);

    const yesterday = new Date(today.getTime())
    yesterday.setDate(today.getDate() - 1);

    const start = Math.floor(yesterday.getTime() / 1000);
    const end = Math.floor(today.getTime() / 1000);

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: events, nextCursor}} = await api.exportEvents({
            pageSize: 100,
            cursor: cursor,
            start: start,
            end: end,
        });

        console.log(events);

        cursor = nextCursor;
        running = events.length > 0;
    }
})();
```

The disadvantage of this approach is that there are no guarantees that the data relative to the specified time window 
have been processed by the time you make the subsequent request. Such cases can happen when events arrive late, 
recent data was not processed fast enough, or during maintenance windows.

#### Exporting Events

The `exportEvents` method exports events from the application associated with the API key, optionally filtered by type 
and a time window relative to the event timestamp.

The following example demonstrates how to export events of a particular type in batches of 100:

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: events, nextCursor}} = await api.exportEvents({
            cursor: cursor,
            pageSize: 100,
        });

        console.log(events);

        cursor = nextCursor;
        running = events.length > 0;
    }
})();
```

#### Exporting Sessions

The `exportSessions` method exports sessions from the application associated with the API key, optionally filtered by 
a time window relative to the session's close time.

The following example demonstrates how to export sessions in batches of 100: 

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: sessions, nextCursor}} = await api.exportSessions({
            cursor: cursor,
            pageSize: 100,
        });

        console.log(sessions);

        cursor = nextCursor;
        running = sessions.length > 0;
    }
})();
```

#### Exporting Users

The `exportUsers` method exports users from the workspace associated with the API key, optionally filtered by 
a time window relative to the user's last modified time.

The following example demonstrates how to export sessions in batches of 100:

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: users, nextCursor}} = await api.exportUsers({
            cursor: cursor,
            pageSize: 100,
        });

        console.log(users);

        cursor = nextCursor;
        running = users.length > 0;
    }
})();
```

## API Reference

This reference documents all the methods available in the Export API.

### constructor

The constructor initializes the Export API client with the API key to use for requests.

#### Signature

The constructor has the following signature:

```ts
constructor(configuration: Configuration);
```

#### Code Sample

Here's a minimal example showing how initialize the client:

```ts
const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));
```

### exportEvents

This method exports events from an application.

#### Signature

The `exportEvents` method has the following signature:

```ts
exportEvents(options: EventExportOptions): Promise<{data: {items: Event[], nextCursor: string}}>;
```

These are the currently supported options:

| Option     | Type     | Description
|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------
| `pageSize` | number   | The maximum number of events to export per request, limited to 1000. By default, 100.
| `cursor`   | string   | The cursor from the previous request to use as a starting point for export. By default, it points to the initial page.
| `start`    | number   | The start timestamp in seconds since epoch relative to the event timestamp, inclusive. By default, the start of the time window is unbounded.
| `end`      | number   | The end timestamp in seconds since epoch relative to the event timestamp, exclusive. By default, the end of the time window is unbounded.
| `events`   | string[] | The types of events to export. By default, include all types listed bellow.

The list possible event types are:

| Event                  | Since Version |
|------------------------|---------------|
| `userSignedUp`         | 1.0.0         |
| `userSignedIn`         | 1.0.0         |
| `userSignedOut`        | 1.0.0         |
| `tabOpened`            | 1.0.0         |
| `tabUrlChanged`        | 1.0.0         |
| `tabVisibilityChanged` | 1.0.0         |
| `locationDetected`     | 1.0.0         |
| `clientDetected`       | 1.0.0         |
| `pageOpened`           | 1.0.0         |
| `pageLoaded`           | 1.0.0         |
| `productViewed`        | 1.0.0         |
| `cartViewed`           | 1.0.0         |
| `cartModified`         | 1.0.0         |
| `checkoutStarted`      | 1.0.0         |
| `orderPlaced`          | 1.0.0         |
| `testGroupAssigned`    | 1.0.0         |
| `nothingChanged`       | 1.0.0         |
| `goalCompleted`        | 1.0.0         |
| `eventOccurred`        | 1.0.0         |

#### Code Sample

Here's a full example showing how to export events:

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: events, nextCursor}} = await api.exportEvents({
            cursor: cursor,
            pageSize: 100,
            start: 1440990000,
            end: 1440990000 + 86_400,
            types: ['productViewed', 'checkoutStarted', 'orderPlaced'],
        });

        console.log(events);

        cursor = nextCursor;
        running = events.length > 0;
    }
})();
```

### exportSessions

This method exports sessions from an application.

#### Signature

The `exportSessions` method has the following signature:

```ts
exportEvents(options: SessionExportOptions): Promise<{data: {items: Session[], nextCursor: string}}>;
```

These are the currently supported options:

| Option     | Type     | Description
|------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------
| `pageSize` | number   | The maximum number of sessions to export per request, limited to 1000. By default, 100.
| `cursor`   | string   | The cursor from the previous request to use as a starting point for export. By default, it points to the initial page.
| `start`    | number   | The start timestamp in seconds since epoch relative to the session's close time, inclusive. By default, the start of the time window is unbounded.
| `end`      | number   | The end timestamp in seconds since epoch relative to the session's close time, exclusive. By default, the end of the time window is unbounded.

#### Code Sample

Here's a full example showing how to export sessions:

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: sessions, nextCursor}} = await api.exportSessions({
            cursor: cursor,
            pageSize: 100,
            start: 1440990000,
            end: 1440990000 + 86_400,
        });

        console.log(sessions);

        cursor = nextCursor;
        running = sessions.length > 0;
    }
})();
```

### exportUsers

This method exports users from a workspace.

#### Signature

The `exportUsers` method has the following signature:

```ts
exportUsers(options: UserExportOptions): Promise<{data: {items: User[], nextCursor: string}}>;
```

These are the currently supported options:

| Option     | Type     | Description
|------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------
| `pageSize` | number   | The maximum number of users to export per request, limited to 1000. By default, 100.
| `cursor`   | string   | The cursor from the previous request to use as a starting point for export. By default, it points to the initial page.
| `start`    | number   | The start timestamp in seconds since epoch relative to the user's last modified time, inclusive. By default, the start of the time window is unbounded.
| `end`      | number   | The end timestamp in seconds since epoch relative to the user's last modified time, exclusive. By default, the end of the time window is unbounded.

#### Code Sample

Here's a full example showing how to export sessions:

```ts
import {Configuration, ExportApi} from '@croct/export';

(async function run(): Promise<void> {
    const api = new ExportApi(new Configuration({apiKey: '00000000-0000-0000-0000-000000000000'}));

    let cursor: string|undefined = undefined;
    let running = true;

    while (running) {
        const {data: {items: users, nextCursor}} = await api.exportUsers({
            cursor: cursor,
            pageSize: 100,
            start: 1440990000,
            end: 1440990000 + 86_400,
        });

        console.log(users);

        cursor = nextCursor;
        running = users.length > 0;
    }
})();
```

## Support

If this documentation has not answered all your questions, don't worry. 
Here are some alternative ways to get help from the Croct community.

### Stack Overflow

Someone else from the community may have already asked a similar question or may be able to help with your problem.

The Croct team will also monitor posts with the "croct" tag. If there aren't any existing questions that help,
please [ask a new one](https://stackoverflow.com/questions/ask?tags=croct%20export).

### GitHub

If you have what looks like a bug, or you would like to make a feature request, please
[open a new issue on GitHub](https://github.com/croct-tech/export-client-node/issues/new/choose).

Before you file an issue, a good practice is to search for issues to see whether others have the same or similar problems.
If you are unable to find an open issue addressing the problem, then feel free to open a new one.

### Slack Channel

Many people from the Croct community hang out on the Croct Slack Group.
Feel free to [join us and start a conversation](https://croct.link/community).

## License

This project is released under the [MIT License](LICENSE).
