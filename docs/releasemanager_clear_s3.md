## releasemanager clear s3

Clear state from the S3 backend

### Synopsis

Clear state from the S3 backend
Run: releasemanager clear --help for more information about clearing
state

```
releasemanager clear s3
```

### Options

```
      --accessKeyID string       An AWS Access Key ID for accessing the S3 bucket, otherwise use the default AWS credential provider chain
      --bucket string            Required. Use this S3 bucket for backend storage
      --region string            The backend S3 bucket's region (default "us-east-1")
      --secretAccessKey string   An AWS Secret Access Key for accessing the S3 bucket, otherwise use the default AWS credential provider chain
      --sessionToken string      An AWS STS Session Token  for accessing the S3 bucket, otherwise use the default AWS credential provider chain
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

- [releasemanager clear](releasemanager_clear.md) - Clear all state

###### Auto generated by spf13/cobra on 6-Aug-2018
