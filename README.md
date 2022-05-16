# extends

> https://github.com/devcontainers/spec/issues/22

##### Executing:

```bash
$ devcontainer merge \
    --workspace-folder .  \
    --sub-folder ./node

```

##### Results in:

```jsonc
{
  "name": "example/project",
  "forwardPorts": [80, 5432, 2222], // <-- Array values are the UNION
  "hostRequirements": {
    "storage": "64gb",
    "memory": "32gb" // <-- Basic types overwrite
  },
  "onCreateCommand": ".devcontainer/on-create-command.sh" // <-- New keys are added
}
```
