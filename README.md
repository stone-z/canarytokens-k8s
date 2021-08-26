# canarytokens-k8s

A [Helm](https://helm.sh/) chart for deploying [`canarytokens`](https://github.com/thinkst/canarytokens) from [Thinkst](https://thinkst.com/) in a Kubernetes cluster.

**Disclaimer:** This is an unofficial repo maintained casually and is not tested or configured for production use.

## Usage

To install `opencanary` in a local `kind` cluster and access the frontend from a local browser:

1. Clone the repo
    ```shell
    git clone https://github.com/stone-z/canarytokens-k8s.git
    cd canarytokens-k8s
    ```
2. (If you don't have a cluster) Start a cluster using [`kind`](https://kind.sigs.k8s.io/):
    ```shell
    kind create cluster
    ```
3. Install `canarytokens-k8s`:
    ```shell
    helm install canarytokens-k8s canarytokens-k8s/
    ```
4. Port-forward the frontend pod to your local machine:
    ```shell
    kubectl port-forward service/frontend 8082:8082
    ```
5. Navigate to `localhost:8082` in your browser.
