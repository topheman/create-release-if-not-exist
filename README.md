# topheman/create-release-if-not-exist

This GitHub Action creates a release if it doesn't exist.

You can pass any arguments you would pass to [`gh release create`](https://cli.github.com/manual/gh_release_create) command that will run if the release doesn't exist.

## Usage

```yaml
jobs:
  release-draft:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Create release draft if not exist
        uses: topheman/create-release-if-not-exist@v1
        with:
          args: "${{ github.ref_name }} --draft --generate-notes"
```

**Note:** Do not forget the `actions/checkout@v4` step, it is needed to have a git repository (use `git` commands in the action).

## Related Actions

- [topheman/update-homebrew-tap](https://github.com/topheman/update-homebrew-tap)

## Used By

- [topheman/webassembly-component-model-experiments](https://github.com/topheman/webassembly-component-model-experiments)
- [topheman/update-homebrew-tap-playground](https://github.com/topheman/update-homebrew-tap-playground)
