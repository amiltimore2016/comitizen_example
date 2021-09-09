# Conventional Changelog

## Steps

Init npm repo

```shell
npm init -y
````

Install dev dependencies

```shell
npm i -D @digitalroute/cz-conventional-changelog-for-jira @semantic-release/gitlab commitizen eslint prettier semantic-release semver
```

add the following to package.json

```json
{
  "scripts": {
    "commit": "git-cz"
  },
  "config": {
    "commitizen": {
      "path": "./node_modules/@digitalroute/cz-conventional-changelog-for-jira"
    }
  }
}
```

For additional customization head over to [cz-conventional-changelog-jira](https://github.com/digitalroute/cz-conventional-changelog-for-jira)

## Commitlint

If using the commitlint js library, the "maxHeaderWidth" configuration property will default to the configuration of the "header-max-length" rule instead of the hard coded value of 72. This can be overwritten by setting the 'maxHeaderWidth' configuration in package.json or the CZ_MAX_HEADER_WIDTH environment variable.

## Husky Setup

Optionally setup husky so github hook gets triggered when committing, your mileage may vary.