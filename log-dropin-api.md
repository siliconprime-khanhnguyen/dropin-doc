# Next release notes:
- Integrate RisingStack/Trace
[PR#475](https://github.com/dropininc/dropin-api-v2/pull/475)

## Deploy notes:
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
