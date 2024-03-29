<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [StatusServiceSetup](./opensearch-dashboards.statusservicesetup.md)

## StatusServiceSetup interface

API for accessing status of Core and this plugin's dependencies as well as for customizing this plugin's status.

<b>Signature:</b>

```typescript
export interface StatusServiceSetup 
```

## Remarks

By default, a plugin inherits it's current status from the most severe status level of any Core services and any plugins that it depends on. This default status is available on the  API.

Plugins may customize their status calculation by calling the  API with an Observable. Within this Observable, a plugin may choose to only depend on the status of some of its dependencies, to ignore severe status levels of particular Core services they are not concerned with, or to make its status dependent on other external services.

## Example 1

Customize a plugin's status to only depend on the status of SavedObjects:

```ts
core.status.set(
  core.status.core$.pipe(
.   map((coreStatus) => {
      return coreStatus.savedObjects;
    }) ;
  );
);
```

## Example 2

Customize a plugin's status to include an external service:

```ts
const externalStatus$ = interval(1000).pipe(
  switchMap(async () => {
    const resp = await fetch(`https://myexternaldep.com/_healthz`);
    const body = await resp.json();
    if (body.ok) {
      return of({ level: ServiceStatusLevels.available, summary: 'External Service is up'});
    } else {
      return of({ level: ServiceStatusLevels.available, summary: 'External Service is unavailable'});
    }
  }),
  catchError((error) => {
    of({ level: ServiceStatusLevels.unavailable, summary: `External Service is down`, meta: { error }})
  })
);

core.status.set(
  combineLatest([core.status.derivedStatus$, externalStatus$]).pipe(
    map(([derivedStatus, externalStatus]) => {
      if (externalStatus.level > derivedStatus) {
        return externalStatus;
      } else {
        return derivedStatus;
      }
    })
  )
);
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [core$](./opensearch-dashboards.statusservicesetup.core_.md) | Observable&lt;[CoreStatus](./opensearch-dashboards.corestatus.md)<!-- -->&gt; | Current status for all Core services. |
|  [dependencies$](./opensearch-dashboards.statusservicesetup.dependencies_.md) | Observable&lt;Record&lt;string, [ServiceStatus](./opensearch-dashboards.servicestatus.md)<!-- -->&gt;&gt; | Current status for all plugins this plugin depends on. Each key of the <code>Record</code> is a plugin id. |
|  [derivedStatus$](./opensearch-dashboards.statusservicesetup.derivedstatus_.md) | Observable&lt;[ServiceStatus](./opensearch-dashboards.servicestatus.md)<!-- -->&gt; | The status of this plugin as derived from its dependencies. |
|  [isStatusPageAnonymous](./opensearch-dashboards.statusservicesetup.isstatuspageanonymous.md) | () =&gt; boolean | Whether or not the status HTTP APIs are available to unauthenticated users when an authentication provider is present. |
|  [overall$](./opensearch-dashboards.statusservicesetup.overall_.md) | Observable&lt;[ServiceStatus](./opensearch-dashboards.servicestatus.md)<!-- -->&gt; | Overall system status for all of OpenSearch Dashboards. |

## Methods

|  Method | Description |
|  --- | --- |
|  [set(status$)](./opensearch-dashboards.statusservicesetup.set.md) | Allows a plugin to specify a custom status dependent on its own criteria. Completely overrides the default inherited status. |

