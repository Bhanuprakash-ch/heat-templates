# heat-templates
Heat Templates


### Requirements
- virtualenv

```
virtualenv tap
. tap/bin/activate
./tap/bin/pip install j2cli
```

### Generate OpenStack Heat template (FullVM)
```
. tap/bin/activate
export  type=fullvm
j2 TAP.yaml.j2  > TAP-FullVM.yaml
```

### Generate Hybrid (OpenStack + Bare Metal) Heat template (Hybrid)
```
. tap/bin/activate
export  type=hybrid
j2 TAP.yaml.j2  > TAP-Hybrid.yaml
```
