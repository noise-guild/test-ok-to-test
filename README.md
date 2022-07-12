# test-ok-to-test

Steps:
* Create a personal access token with repo access from https://github.com/settings/tokens
* Create a repository secret called `PERSONAL_ACCESS_TOKEN` with the contents of the token
* Create a repository secret called `VERY_SECRET` with `secret content` as value to test.
* Create a [ok-to-test](./.github/workflows/ok-to-test.yml) workflow.
* Create an [unprotected](./.github/workflows/unprotected.yml) workflow, it will always run on pull requests and won't have access to secrets.
* Create a [protected](./.github/workflows/protected.yml) workflow, it will run only after an user with write access to the repo comments `/ok-to-test sha=...` in a pull request and will have access to secrets.

test...
test...
