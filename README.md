# renovate-helmfile-reproductions

To validate helmfile you can execute:
```bash
helmfile --log-level debug -e beta template
```

To validate Renovate please run in a repo root:
```bash
export RENOVATE_PLATFORM=github
export RENOVATE_TOKEN="YOUR_GITHUB_TOKEN"
export RENOVATE_AUTODISCOVER='false'
export LOG_LEVEL=debug

renovate
```