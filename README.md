## kubectl-druid-plugin
- Kubectl plugin to simplify druid CR operations.

## Getting Started
- NOTE: go version 1.15
- go build -o kubectl-druid
- mv kubectl-druid /usr/local/bin
- kubectl druid --help

## Commands

- List All Druid CR's in a k8s cluster
```
kubectl druid list
```

- List Druid CR's in a namespace
```
kubectl druid list --namespace <namespace>
```

- Get Druid Nodes's in a namespace for a specific cr
```
kubectl druid get nodes --cr <cr>--namespace <namespace>
```

- Scale Druid Replicas for a specific druid cr node in a namespace
```
kubectl druid scale --cr <cr> --namespace <namespace> --node middlemanager --replicas 4
```

- Update Image for a specific druid CR node in namespace
```
kubectl druid update --CR <CR> --image <image> --namespace <namespace> --node broker
```

- Patch Operation of CR Flags
```
kubectl druid patch --cr <cr> --namespace <namespace> --deleteOrphanPvc true
kubectl druid patch --cr <cr> --namespace <namespace> --rollingDeploy true
```
