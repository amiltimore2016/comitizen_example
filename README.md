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

## Install as Dev dependencies the following

* @commitlint/cli
* @commitlint/config-conventional
* commitizen
* commitlint-config-jira
* commitlint-plugin-jira-rules
* cz-conventional-changelog-custom-format
* husky
* standard-version

```shell
  npm i -D commitlint/cl commitlint/config-conventional commitizen commitlint-config-jira commitlint-plugin-jira-rules cz-conventional-changelog-custom-format husky standard-version
```

## Create commitlint.config.js

```shell
   echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

## Add scritps to package.json

```json
{
  "scripts": {
    "commit": "cz",
    "release": "standard-version"
  },
...
```

## Add the husky configuration parameters in your package.json

```json
   "husky": {
    "pre-commit": "npm run lint",
    "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
   },
```

## Add your .versionrc.json file so the urls can be updated in CHANGELOG.md

```json
  {
    "commitUrlFormat": "https://github.com/amiltimore2016/comitizen_example/commits/",
    "issueUrlFormat": "https://jira.bookinggo.io/browse/"
  }
```

## yadadayada