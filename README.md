# Quick start

- One-click to setup a Kubernetes cluster with single node:

  ```shell
  curl -sfL https://get.bare-k8s.io | sh -
  ```

- These components will be installed:

  - Datastore (etcd): distributed key-value store
  - Control plane: manage cluster state, schedule pods to nodes
  - Kubelet: agent running in each node to manage node with control plane config
  - Container runtime: manage containers

- Congratulation! A fully-functional K8s cluster is up. Next step is to add more server or agent nodes on your demand.

  ```
  Installing...

  Server started at https://myserver:6443
  Server token is mytoken
  Server secret is mysecret

  Done!
  ```

# Install additional nodes

- One-click to install an agent node, and register to a running server node:

  ```shell
  curl -sfL https://get.bare-k8s.io | B8S_URL=https://myserver:6443 B8S_TOKEN=mytoken sh -
  ```

- One-click to install a server node for High Availability:

  ```shell
  curl -sfL https://get.bare-k8s.io | B8S_URL=https://myserver:6443 B8S_SECRET=mysecret sh -
  ```
