# Integration Guide

## 1. Create a personal access token

Create a GitHub Personal Access Token with `repo` and `workflow` scopes, then save it in the generated repository as:

- Secret name: `PAT_TOKEN`

## 2. Trigger generation

Run the workflow manually from the Actions tab, or later trigger it from the proto repository with `repository_dispatch`.

## 3. Create a release tag manually

After the first successful generation, create a release like `v1.0.0` in:

- `https://github.com/ilarvne/ap2-medical-protos-go/releases`

## 4. Use from a Go service

```bash
go get github.com/ilarvne/ap2-medical-protos-go@v1.0.0
```

Example import:

```go
import appointmentv1 "github.com/ilarvne/ap2-medical-protos-go/appointment/v1"
```
