## Experiments with a Turing Pi 2 

preliminary experiments with a [Turing Pi 2](https://turingpi.com/product/turing-pi-2/) running a [k3s](https://k3s.io/) cluster.

[tpipoweron.yaml](tpipoweron.yaml) powers on the four nodes of the Turing Pi board. It then waits for the OS on each node to present an SSH service.

[shutdown_cluster.yaml](shutdown_cluster.yaml) shuts down and powers down the worker nodes and then shuts down and powers down the cluster controllers. The playbook waits for the node to stop responding to pings. It then waits an additional thirty seconds before instructing the Turing Pi to power off the node.