# ProxyConfig

Proxy config. Null = disable proxy. Object = enable with mode.


## Supported Types

### `operations.ProxyConfigResidential`

```typescript
const value: operations.ProxyConfigResidential = {
  mode: "residential",
  country: "Ecuador",
};
```

### `operations.ProxyConfigIsp`

```typescript
const value: operations.ProxyConfigIsp = {
  mode: "isp",
  country: "Bolivia",
  staticIp: "<value>",
  staticPort: 277356,
};
```

