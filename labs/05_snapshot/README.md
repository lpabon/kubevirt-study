
https://kubevirt.io/user-guide/operations/snapshot_restore_api

I could not do an online snapshot of the fedora VM which had one hotplug
persistent volume. Once I powered it off, the snapshot worked.

Also, the ssh exposed service was not created for vm2


# NOTE on ssh

When exposing vm2:

```
virtctl expose vmi vm2 --name=vm2-ssh --port=22  --type=NodePort
```

It sometimes sshs to vm1. That is because they both have the same labels, and
therefore, Kubernetes service is loadbalancing them. To solve this issue, we
need to create a new label for vm2 then redo the service.

