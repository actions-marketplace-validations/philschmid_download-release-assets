# Download Release Assets from Github

This action downloads an Assets from a Github release. Private repos are supported.

## Inputs

### `repository`

The `owner/repository`. Defaults to the current repository.

### `release`

The release version to fetch from. Default `"latest"`. If not `"latest"`, this has to be in the form `tags/<tag_name>` or `<release_id>`.

### `asset_name`

**Required** The name of the Asset in the release, which should be downloaded.

### `github_token`

A Github Access Token (Optional Personal Access Token) to access repository.

## Outputs

### `result`

The state of the action, if the file could be downloaded successfully

## Example usage

# Smallest Configuration

```yaml
uses: philschmid/download-release-assets@master
with:
  file: packages.zip
  token: ${{ secrets.GITHUB_TOKEN }}
```

# Custom Repository Configuration

```yaml
uses: philschmid/download-release-assets@master
with:
  repository: philschmid/frontend-applikation
  file: packages.zip
  token: ${{ secrets.GITHUB_TOKEN }}
```

# Custom Version Configuration

```yaml
uses: philschmid/download-release-assets@master
with:
  version: latest
  file: packages.zip
  token: ${{ secrets.GITHUB_TOKEN }}
```

# Custom Version and Repository Configuration

```yaml
uses: philschmid/download-release-assets@master
with:
  repository: philschmid/frontend-applikation
  version: latest
  file: packages.zip
  token: ${{ secrets.GITHUB_TOKEN }}
```
