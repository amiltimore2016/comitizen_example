# comitizen_example

## Setup

* Create a folder calle comitizen_example.

```shell
mkdir comitizen_example
```

* Change into folder and initilize npm project.
  
```shell
   cd comitizen_example
   npm init -y
```

* Install as Dev dependencies the following
  * @commitlint/cli
  * @commitlint/config-conventional
  * commitizen
  * commitlint-config-jira
  * commitlint-plugin-jira-rules
  * cz-conventional-changelog-custom-format
  * husky
  * standard-version

* Create commitlint.config.js

```shell
   echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

