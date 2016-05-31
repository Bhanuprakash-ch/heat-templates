# heat-templates
Heat Templates


## Requirements

### Ubuntu/Debian
- python-virtualenv
- python-dev
- python-pip

```
virtualenv tap
. tap/bin/activate
pip install -r requirements.txt
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
