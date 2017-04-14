# Black Duck CoPilot pip/Circle CI Example

[![CircleCI](https://img.shields.io/circleci/project/github/BlackDuckCoPilot/example-pip-circle/master.svg)](https://circleci.com/gh/BlackDuckCoPilot/example-pip-circle)

Shows a working setup for using the Black Duck CoPilot integration to analyze the risk of project dependencies

## Circle CI Setup

The `circle.yml` file has been modified to upload the generated data to Black Duck CoPilot:

```yaml
test:
  post:
    - pip install hub-pip==1.0.0
    - python setup.py hub_pip --DeployHubBdio=false
    - bash <(curl -s https://copilot.blackducksoftware.com/bash/circle) ./build/blackduck/*.jsonld
```


