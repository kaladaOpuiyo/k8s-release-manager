## releasemanager import

Import Helm release state

### Synopsis

Release Manager Import will retrieve state from the configured
backend and install all exported releases to the current Kubernetes cluster.

We should avoid introducing scenarios where an imported Release Manager release
is configured to write to the same backend path as an existing
Release Manager in a different cluster. If a Release Manager release is stored
in the remote state, and --new-path is not set, this command will fail. If
you're really sure that this is an operation you want to perform (it probably
isn't), you can set --force to ignore safety checks.

Import is designed to fail if a release already exists with the same name as
a stored release. This is by design. If you to overwrite an existing release,
you should delete it first using helm delete --purge.

### Options

```
      --atomic                         if set, the installation process deletes the installation on failure. (default true)
      --create-namespace               create the release namespace if not present (default true)
      --exclude-namespaces strings     A list of namespaces to exclude. The default behavior is to import all namespaces
      --force                          Skip safety checks
      -h, --help                           help for import
      --namespace string               Specify a specific namespace to import releases from. Required if 'target-namespace' specified
      --new-path string                When installing an exported Release Manager release, update the value of --path
      --release-timeout int            The time, in seconds, to wait for an individual Helm release to install (default 300)
      --replace                        re-use the given name, only if that name is a deleted release which remains in the history. This is unsafe in production (default true)
      --target-namespace string        Specify a new namespace to import releases to
      --threads int                    The maximum number of threads to use for installing releases (default 50)
      --update-values stringToString   Specify a mapping of values to update when importing releases. Overrides apply to all releases for which a given value is already set, but will not insert the value if it doesn't already exist (default [])
      --wait                           if set, will wait until all Pods, PVCs, Services, and minimum number of Pods of a Deployment,    StatefulSet, or ReplicaSet are in a ready state before marking the release as successful (default true)
```

### Options inherited from parent commands

```
      --config string             Set a custom configuration path
      --debug                     Enable debugging output
      --dry-run                   Print planned actions without making any modifications
      --kubeconfig string         Use this kubeconfig path, otherwise use the environment variable KUBECONFIG or ~/.kube/config
      --kubecontext string        Use this kube context, otherwise use the default
      --path string               Required. Use this path within the backend for state storage
      -v, --verbose                   Enable verbose output
```

### SEE ALSO

- [releasemanager](releasemanager.md) - Release Manager is a tool for importing and exporting Helm release state
- [releasemanager import local](releasemanager_import_local.md) - Import state from the local backend
- [releasemanager import s3](releasemanager_import_s3.md) - Import state from the S3 backend

###### Auto generated by spf13/cobra on 6-Aug-2018
