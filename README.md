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
### Setting TAP version
TAP version should by exported before template generation.
Version string should by identical as tag or branch name on ansible-playbooks repo.

Setting `tap_version` is mandatory. Examples:
- `export tap_version=v0.7.1` will use code taged as `v0.7.1`
- `export version=develop` will use code from branch `develop`

### Generate OpenStack Heat template (FullVM)
```
. tap/bin/activate
export tap_version=v0.7.1
export type=fullvm
j2 TAP.yaml.j2  > TAP-FullVM.yaml
```

### Generate Hybrid (OpenStack + Bare Metal) Heat template (Hybrid)
```
. tap/bin/activate
export tap_version=v0.7.1
export type=hybrid
j2 TAP.yaml.j2  > TAP-Hybrid.yaml
