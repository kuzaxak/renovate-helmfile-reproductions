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

Error:
```
DEBUG: Failed to parse helmfile helmfile.yaml (repository=kuzaxak/renovate-helmfile-reproductions)
       "err": {
         "name": "YAMLException",
         "reason": "expected a single document in the stream, but found more",
         "message": "expected a single document in the stream, but found more",
         "stack": "YAMLException: expected a single document in the stream, but found more\n    at load (/usr/local/lib/node_modules/renovate/node_modules/js-yaml/lib/js-yaml/loader.js:1622:9)\n    at Object.safeLoad (/usr/local/lib/node_modules/renovate/node_modules/js-yaml/lib/js-yaml/loader.js:1637:10)\n    at Object.extractPackageFile (/usr/local/lib/node_modules/renovate/dist/manager/helmfile/extract.js:37:33)\n    at Object.extractPackageFile (/usr/local/lib/node_modules/renovate/dist/manager/index.js:64:13)\n    at Object.getManagerPackageFiles (/usr/local/lib/node_modules/renovate/dist/workers/repository/extract/manager-files.js:41:41)\n    at async /usr/local/lib/node_modules/renovate/dist/workers/repository/extract/index.js:42:30\n    at async Promise.all (index 0)\n    at async Object.extractAllDependencies (/usr/local/lib/node_modules/renovate/dist/workers/repository/extract/index.js:41:28)\n    at async Object.extract (/usr/local/lib/node_modules/renovate/dist/workers/repository/process/extract-update.js:75:24)\n    at async Object.extractDependencies (/usr/local/lib/node_modules/renovate/dist/workers/repository/process/index.js:60:41)\n    at async Object.renovateRepository (/usr/local/lib/node_modules/renovate/dist/workers/repository/index.js:64:56)\n    at async Object.start (/usr/local/lib/node_modules/renovate/dist/workers/global/index.js:77:13)\n    at async /usr/local/lib/node_modules/renovate/dist/renovate.js:28:24"
       },
       "fileName": "helmfile.yaml"
DEBUG: Found 0 package file(s) (repository=kuzaxak/renovate-helmfile-reproductions)
```