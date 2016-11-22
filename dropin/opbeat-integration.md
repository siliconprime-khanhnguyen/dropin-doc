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
PR: [PR#89](https://github.com/dropininc/dropin-web-v2/pull/89)

### Deployment status:
- Dev: Done
- QA: Done
- Staging: Config updated - Waiting for deploy
- Staging Demo: New
- Production: New

### Deploy notes:
- Need to update config in `config/web-env/`:
```
module.exports = {
  ...
  opbeat: {
    orgId: 'bd944329871a4e47a2acecdcc36c810a',
    appId: '9a0c54f310'
  },
  ...
}
```