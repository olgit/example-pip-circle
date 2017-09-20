# Black Duck CoPilot pip/Circle CI Example

[![CircleCI](https://img.shields.io/circleci/project/github/BlackDuckCoPilot/example-pip-circle/master.svg)](https://circleci.com/gh/BlackDuckCoPilot/example-pip-circle) [![Black Duck Security Risk](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-pip-circle/branches/master/badge-risk.svg)](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-pip-circle/branches/master)

Shows a working setup for using Black Duck CoPilot to analyze the risk of project dependencies

## Circle CI Setup
The `circle.yml` file has been modified to upload generated dependency data to CoPilot:
```yaml
test:
  post:
    - bash <(curl -s https://copilot.blackducksoftware.com/ci/circle/scripts/upload)
```
