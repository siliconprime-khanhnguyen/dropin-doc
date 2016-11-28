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
Dev          | Trace - Deployed | Trace
QA           | New Relic - Deployed | New Relic
QA research  | NR - Deployed | NR
Staging      | NR - Pre-Deployed | NR
Staging Demo | T - Config deployed (Code will be updated in future release) | T
Production   | NR - Config deployed (Code will be updated in future release) | NR

## API
### Pull Requests
- develop -
[PR#483](https://github.com/dropininc/dropin-api-v2/pull/483),
[PR#488](https://github.com/dropininc/dropin-api-v2/pull/488)
- qa-release - [PR#487](https://github.com/dropininc/dropin-api-v2/pull/487)
- qa-research - no PR
- staging - [PR#489](https://github.com/dropininc/dropin-api-v2/pull/489)
- demo - no PR, code will be updated in future release
- production - no PR, code will be updated in future release

