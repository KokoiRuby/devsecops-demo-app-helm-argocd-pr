## Overview

**This helm repo is a twin repo that adapts to ArgoCD [ApplicationSet](https://argo-cd.readthedocs.io/en/latest/user-guide/application-set/) with [PR generator](https://argo-cd.readthedocs.io/en/stable/operator-manual/applicationset/Generators-Pull-Request/). Please check brother repo [here](https://github.com/KokoiRuby/devsecops-demo-app-helm).**

## Install

An out-of-box Kubernetes cluster environment is required. Try [kind](https://kind.sigs.k8s.io/). 👈 Then set up an [ingress](https://kind.sigs.k8s.io/docs/user/ingress/) controller for it.

```bash
# install
helm install devsecops-demo-app .
```

Add local DNS resolution.

```bash
# Windows: C:\Windows\System32\drivers\etc
# WSL: sudo vim /etc/hosts
127.0.0.1 demo-app.default.devsecops.yukanyan.us.kg
```

## Verify

http://demo-app.default.devsecops.yukanyan.us.kg/foo

http://demo-app.default.devsecops.yukanyan.us.kg/bar

```bash
# or in command line terminal
curl demo-app.default.devsecops.yukanyan.us.kg/foo
curl demo-app.default.devsecops.yukanyan.us.kg/bar
```

## Uninstall

```bash
helm uninstall devsecops-demo-app
```

