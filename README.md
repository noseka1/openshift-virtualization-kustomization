# Kustomization for Deploying Red Hat OpenShift Virtualization (KubeVirt)

Red Hat OpenShift Virtualization documentation is part of Red Hat OpenShift Container Platform product documentation and it can be found [here](https://access.redhat.com/documentation/en-us/openshift_container_platform).

## Deploying Operator

```
$ oc apply --kustomize openshift-virtualization-operator/base
```

## Deploying OpenShift Virtualization Instance

```
$ oc apply --kustomize openshift-virtualization-instance/base
```
