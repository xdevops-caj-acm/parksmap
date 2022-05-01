[TOC]

# parksmap

## Images

```bash
quay.io/openshiftroadshow/parksmap:latest
```

## Create application via commands:
```bash
# create project
oc new-project will-test

# create application
oc new-app -n will-test \
  --image=quay.io/openshiftroadshow/parksmap:latest \
  --name=parksmap \
  --labels=app=workshop,component=parksmap,role=frontend

# add labels for "Application name" and "Runtime icon"
oc label deployment parksmap "app.kubernetes.io/part-of"=workshop "app.openshift.io/runtime"=spring-boot

# create an edge route
oc create route edge parksmap --service=parksmap

```

## Kustomize

- <https://kubernetes.io/docs/tasks/manage-kubernetes-objects/kustomization/>
- <https://github.com/kubernetes-sigs/kustomize>

## ACM Lab

- <https://github.com/xdevops-caj-acm/rhacmgitopslab>
