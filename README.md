# SemVer Bump Action

<p align="center">
  <a href="https://github.com/dinosu-actions/semver-bump/actions"><img alt="javscript-action status" src="https://github.com/dinosu-actions/semver-bump/workflows/units-test/badge.svg"></a>
</p>

This action reads a file for the semver version and increment it based on the release type.

## Inputs

### `path`
**Required** The path to the file containing the semantic version.

### `release-type`
**Required** The type of release. Acceptable values are: `major`, `minor`, `patch`

### `pre-release`
The pre-release label. This will still cause a bump to the appropriate semver component specified by `release-type`.

## Outputs

### `previous-version`
This is the version stored in the file at time of execution.

### `version`
This is the version we are moving to.

## Usage

You can now consume the action by referencing the v1 branch

```yaml
uses: dinosu-actions/semver-bump@v1.0
with:
  path: ./path/to/VERSION
  release-type: patch
  pre-release: my-pre-release-label
```

See the [actions tab](https://github.com/dinosu-actions/semver-bump/actions) for runs of this action! :rocket:
