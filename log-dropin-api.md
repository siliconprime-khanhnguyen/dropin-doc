# Rising stack integration notes:
## API
PR: [PR#475](https://github.com/dropininc/dropin-api-v2/pull/475)

### Deployment status:
Dev: Done

QA: New

Staging: Waiting for approval [DESKTOP-737](https://dropin.atlassian.net/browse/DESKTOP-737)

### Deploy notes:
- Need to update config:
```
module.exports = {
  ...
  risingStack: {
    trace: {
      serviceName: '<service name>',
      apiKey: '<api key>'
    }
  },
  ...
}
```
## Web
PR: [PR#87](https://github.com/dropininc/dropin-web-v2/pull/87)

### Deployment status:
Dev: In-progress

QA: New

Staging: Waiting for approval [DESKTOP-736](https://dropin.atlassian.net/browse/DESKTOP-736)

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
