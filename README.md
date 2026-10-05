# OpenShell `.project`

CNCF project metadata for [OpenShell](https://github.com/NVIDIA/OpenShell).

| File | Purpose |
| --- | --- |
| [`project.yaml`](project.yaml) | Project identity, maturity, governance, security, and landscape metadata |
| [`maintainers.yaml`](maintainers.yaml) | Maintainer roster used for CNCF resource provisioning |

Both files follow the CNCF [`.project` schema](https://github.com/cncf/automation/blob/main/utilities/dot-project/SCHEMA.md) (version `1.0.0`).

## Making changes

Open a pull request. CI validates both files against the schema, and merges to
`main` that touch `project.yaml` open a pull request against
[`cncf/landscape`](https://github.com/cncf/landscape) with the updated entry.

The maintainer roster here must stay in sync with
[`MAINTAINERS.md`](https://github.com/NVIDIA/OpenShell/blob/main/MAINTAINERS.md)
in the main repository. Maintainer changes follow the process in
[`GOVERNANCE.md`](https://github.com/NVIDIA/OpenShell/blob/main/GOVERNANCE.md#becoming-a-maintainer).

To validate locally:

```shell
git clone https://github.com/cncf/automation.git
go run ./automation/utilities/dot-project/cmd/validator -repo-root .
```
