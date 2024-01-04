# go-install

## Usage

### Specify by version
```
- name: Setup Go
  uses: exzeo-devops/action-workflows/.github/actions/go-install@main
  with:
    version: "1.24.1"
```

If no version is provided, will use stable version, if no .go-version is provided, otherwise, will be determined by the version in .go-version

Version is ignored if .go-version file exists

### Example .go-version file contents
```
1.24.1
```