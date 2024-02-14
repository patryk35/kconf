# kconf - Taskfile with scripts to configure local tools used across multiple K8S cluster

# How to use?

1. Create appropriate config file in path `KCONF_CONFIG_PATH` (deafult: `~/.kconf/config.yaml`):
   - ~~manually using example example: examples/example_config.yaml~~
   - `task init_minimal_config KUBE_CONTEXT_NAME=...`
2. Set context to your cluster e.g. `kubie ctx minikube`
3. Run

```commandline
task setup && source env_source.tmp
```

# Requirements

- Taskfile 3.27.0 or newer
- yq 4.x.x
- kubectl (TODO: refactor script to use yq or ?)

Optional:

- kubiectx or kubeswitch or kubens/kubectx

