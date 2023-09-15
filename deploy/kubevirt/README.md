
## Feature Gates

Edit the folloging:

```

kubectl edit -n kubevirt kubevirt kubevirt

Then add the following
spec:
  certificateRotateStrategy: {}
  configuration:
    developerConfiguration:
      featureGates:
        - HotplugVolumes
        - ExpandDisks
        - Snapshot
        - HostDevices
        - HostDisk
```

