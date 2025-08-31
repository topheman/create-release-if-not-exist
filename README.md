# topheman/create-release-if-not-exist

This GitHub Action runs a script to create a release draft if it doesn't exist.

## Usage

```yaml
jobs:
  release-draft:
    runs-on: ubuntu-latest
    steps:
      - name: Create release draft if not exist
        uses: topheman/create-release-if-not-exist@v1
        with:
          args: "${{ github.ref_name }} --draft --generate-notes"
        env:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
