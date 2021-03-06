## kops get

Get one or many resources.

### Synopsis


Display one or many resources. 

  * cluster  
  * instancegroup  
  * secret  
  * federation

```
kops get
```

### Examples

```
  # Get all resource in a single cluster as yaml
  kops get --name k8s-cluster.example.com -o yaml
  
  # Get all clusters in a state store
  kops get clusters
  
  # Get a cluster
  kops get cluster k8s-cluster.example.com
  
  # Get a cluster YAML cluster spec
  kops get cluster k8s-cluster.example.com -o yaml
  
  # Get an instancegroup
  kops get ig --name k8s-cluster.example.com nodes
  
  # Get a secret
  kops get secrets kube -oplaintext
  
  # Get the admin password for a cluster
  kops get secrets admin -oplaintext
```

### Options

```
  -o, --output string   output format.  One of: table, yaml, json (default "table")
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --config string                    config file (default is $HOME/.kops.yaml)
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files (default false)
      --name string                      Name of cluster
      --state string                     Location of state storage
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO
* [kops](kops.md)	 - kops is Kubernetes ops.
* [kops get clusters](kops_get_clusters.md)	 - Get one or many clusters.
* [kops get federations](kops_get_federations.md)	 - Get federation.
* [kops get instancegroups](kops_get_instancegroups.md)	 - Get one or many instancegroups
* [kops get secrets](kops_get_secrets.md)	 - Get one or many secrets.

