# Post-Quantum Blockchain local deployment

## Pre-requisites
- Docker
- Yarn
- [Kurtosis CLI](https://docs.kurtosis.com/install)
    - Start Kurtosis engine after installation using : ``` kurtosis engine start ```
- [The NEAR-CLI Post-Quantum variant](https://github.com/Post-Quantum-Team/Post-Quantum-near-cli)
    - [The Rust NEAR-CLI Post-Quantum variant can also be used](https://github.com/Post-Quantum-Team/Post-Quantum-Near-CLI-RS)


## Setup

Launch your Post-Quantum Kurtosis NEAR Module in four easy steps!

### 1 - Launch Docker

### 2 - Copy the [Post-Quantum Kurtosis NEAR Module](https://github.com/Post-Quantum-Team/Post-Quantum-near-kurtosis-module/blob/master/launch-local-near-cluster.sh) launch script by running the following:
```
curl -o ~/launch-local-pqnear-cluster.sh https://raw.githubusercontent.com/Post-Quantum-Team/Post-Quantum-near-kurtosis-module/master/launch-local-near-cluster.sh -L
```

### 3 - Grant write permission to the script file you just downloaded:
```
chmod +x ~/launch-local-pqnear-cluster.sh
```

### 4 - Launch the Kurtosis NEAR Module:
If you're running the NEAR-in-Kurtosis cluster on your local machine:
```
~/launch-local-near-cluster.sh
```
If you're running your NEAR-in-Kurtosis cluster on a machine you intend to access remotely, replace "1.2.3.4" with the IP address of the machine you're running the cluster on:
```
~/launch-local-near-cluster.sh --execute-params '{"backendIpAddress":"1.2.3.4"}'
```

To get more details about the Kurtosis cluster:
```
kurtosis enclave inspect near
```

For the rest of the tutorial, please refer to the [NEAR Kurtosis documentation](https://docs.near.org/develop/testing/kurtosis-localnet).

