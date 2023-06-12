# eth-testnet-index
An index of packages and examples for getting started with private Ethereum testnets using Kurtosis.

### Available Testnet Components

| Component | Type | URL | Import Statement |
| --- | --- | --- | --- |
| Geth | EL client | [Github](https://github.com/kurtosis-tech/eth-network-package/blob/main/src/el/geth/geth_launcher.star) | `import_module(https://github.com/kurtosis-tech/eth-network-package/src/el/geth/geth_launcher.star)` |
| Lighthouse | CL client | [Github](https://github.com/kurtosis-tech/eth-network-package/blob/main/src/cl/lighthouse/lighthouse_launcher.star) | `import_module(https://github.com/kurtosis-tech/eth-network-package/src/cl/lighthouse/lighthouse_launcher.star)` |
| MEV Boost | MEV Infra | TBD | TBD |

### Compose Testnet Package Examples

| Package | URL | Import Statement |
| --- | --- | --- |
| Geth + Lighthouse | [Github](https://github.com/kurtosis-tech/eth-network-package/blob/main/src/el/geth/geth_launcher.star) | `import_module(https://github.com/kurtosis-tech/eth-network-package/src/el/geth/geth_launcher.star)` |
| Geth + Lighthouse + MEV Infra | TBD | TBD |

### Roadmap

- [ ] Turn tables into pretty-formatted blocks so people can click-to-copy import statements
- [ ] Add README for quick start + install instructions to Kurtosis
- [ ] Fill out components with each available EL and CL client
- [ ] Add example testnet packages for flexible EL/CL pairings
- [ ] Fill out componenets with each MEV infra component
- [ ] Add example testnet package for MEV infra + EL/CL pairings
