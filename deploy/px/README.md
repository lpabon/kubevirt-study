# Portworx

Make sure to set a default storageclass:

```
kubectl patch storageclass px-csi-replicated  -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
```


