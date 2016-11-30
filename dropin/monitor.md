# Monitor tools integration log

## Deployment status
Status: 
- New
- -> Config updated
- -> PR created
- -> Code updated/PR merged
- -> Config deployed
- -> Pre-Deploy(Wait for deploy confirmation)
- -> Deployed

Env          | API | Web
-------------|-----|-----
Local        | x | x
Dev          | Trace - Deployed | Trace - Deployed (no change)
QA           | New Relic - Deployed | New Relic - Deployed
QA research  | NR - Deployed | NR - Deployed
Staging      | NR - Deployed | NR - Deployed
Staging Demo | T - Config deployed (Code will be updated in future release) | T - Config deployed (Code will be updated in future release)
Production   | NR - Config deployed (Code will be updated in future release) | NR - Config deployed (Code will be updated in future release)

## API
### Pull Requests
- develop -
[PR#483](https://github.com/dropininc/dropin-api-v2/pull/483),
[PR#488](https://github.com/dropininc/dropin-api-v2/pull/488)
- qa-release - [PR#487](https://github.com/dropininc/dropin-api-v2/pull/487)
- qa-research - no PR
- staging - [PR#489](https://github.com/dropininc/dropin-api-v2/pull/489)
- demo - no PR, code will be updated in future release
- prod-release - no PR, code will be updated in future release

### Code changes
- remove opbeat
- change trace@risingStack to only run if has config
- add newrelic. only run if has config

### Config changes
- remove opbeat
- Enable/Disable risingStack & newrelic for each env

## Web
### Pull Requests
- develop - 
[PR#99](https://github.com/dropininc/dropin-web-v2/pull/99),
[PR#101](https://github.com/dropininc/dropin-web-v2/pull/101)
- qa - 
[PR#100](https://github.com/dropininc/dropin-web-v2/pull/100),
[PR#102](https://github.com/dropininc/dropin-web-v2/pull/102)
- qa-research - no PR
- staging - [PR#103](https://github.com/dropininc/dropin-web-v2/pull/103)
- staging-demo - no PR, code will be updated in future release
- prod-clone - no PR, code will be updated in future release

### Code changes
- remove opbeat
- change trace@risingStack to only run if has config
- add newrelic. only run if has config

### Config changes
- Enable/Disable risingStack & newrelic for each env
