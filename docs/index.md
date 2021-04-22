Drone plugin to handle Git operations. You are able to customize some repository
cloning or also commit and push some change as part of the pipeline.

## Examples

```yaml
kind: pipeline
name: default

steps:
- name: step name
  image: dronehippie/git:1
  settings: []
```

## Parameters

dummy
: dummy
