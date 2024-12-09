###### Understanding Permissions & Potential Issues

- You can control which kind of permissions a workflows has.
- Ex. Whether, a workflow is able to interact with issue of repositroy or with a code.

- Bydefault, our workflows has full permissions.

- Permissions are managed at Job level & each seperate Job level.

#### Issues Actions Permissions at Job level.
```
name: Label Issues (Permissions Example)
on:
  issues:
    types:
      - opened
permissions:
    issues: write
jobs:
  assign-label:
    runs-on: ubuntu-latest
```
#### Issues Actions Permissions at Each seperate job level.
```
name: Label Issues (Permissions Example)
on:
  issues:
    types:
      - opened
jobs:
  assign-label:
    permissoions:
        issues: write
    runs-on: ubuntu-latest
```

#### Access Permissions.
```
permissions:
  actions: read|write|none
  attestations: read|write|none
  checks: read|write|none
  contents: read|write|none
  deployments: read|write|none
  id-token: write|none
  issues: read|write|none
  discussions: read|write|none
  packages: read|write|none
  pages: read|write|none
  pull-requests: read|write|none
  repository-projects: read|write|none
  security-events: read|write|none
  statuses: read|write|none
```