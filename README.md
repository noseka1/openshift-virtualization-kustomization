# Kustomization for Deploying Red Hat OpenShift Virtualization (KubeVirt)

Red Hat OpenShift Virtualization documentation is part of Red Hat OpenShift Container Platform product documentation. It can be found at [access.redhat.com](https://access.redhat.com/documentation/en-us/openshift_container_platform) or [docs.openshift.com](https://docs.openshift.com/container-platform/4.7/virt/about-virt.html).

## Deploying Operator

Deploy OpenShift Virtualization operator:

```
$ oc apply --kustomize openshift-virtualization-operator/base
```

Make sure that the csvs deployed successfully:

```
$ oc get csv --namespace openshift-cnv
NAME                                      DISPLAY                    VERSION   REPLACES                                  PHASE
kubevirt-hyperconverged-operator.v2.6.5   OpenShift Virtualization   2.6.5     kubevirt-hyperconverged-operator.v2.6.4   Succeeded
```

## Deploying OpenShift Virtualization Instance

Create OpenShift Virtualization instance:

```
$ oc apply --kustomize openshift-virtualization-instance/base
```

## Using OpenShift Virtualization

Download OpenShift Virtualization CLI (*virtctl*) from [GitHub](https://github.com/kubevirt/kubevirt/releases).
