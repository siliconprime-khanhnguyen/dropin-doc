# Opbeat integration notes
## API
PR: [PR#477](https://github.com/dropininc/dropin-api-v2/pull/477)

### Deployment status:
- Dev: Done
- QA: Done
- Staging: Config updated - Waiting for deploy
- Staging Demo: New
- Production: New

### Deploy notes:
- Need to update config:
```
module.exports = {
  ...
  opbeat: {
    appId: '<app ID>',
    organizationId: '<org ID>',
    secretToken: '<secret token>'
  },
  ...
}
```
## Web
PR: [PR#87](https://github.com/dropininc/dropin-web-v2/pull/87)

### Deployment status:
- Dev: Done
- QA: Done
- Staging: Config updated - Waiting for deploy [DESKTOP-736](https://dropin.atlassian.net/browse/DESKTOP-736)
- Staging Demo: Config updated
- Production: Config updated

### Deploy notes:
- Need to update config:
```
{
  ...
  "risingStack": {
    "trace": {
      "serviceName": "<service name>",
      "apiKey": "<api key>"
    }
  },
  ...
}
```
