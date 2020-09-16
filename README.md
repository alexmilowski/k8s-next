# k8s-next

A set of utilities for K8s workflows

## An example

Wait for a Redis Enterprise cluster to be the status "Running":

```
python -m k8snext --use-config --namespace redis redisenterpriseclusters test status.state --value Running --wait
echo $?
```

After 60 seconds, the command will return an exit status where zero is success
(i.e., the cluster is in state "Running"). The time period can be controlled
by the --period and --limit parameters.
