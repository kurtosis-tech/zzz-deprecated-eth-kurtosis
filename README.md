# eth-kurtosis

An index of packages and examples for getting started with private Ethereum testnets using Kurtosis.

### Available Testnet Components

| Component | Type | URL | Import Statement |
| --- | --- | --- | --- |
| Geth | EL client | [Github](https://github.com/kurtosis-tech/geth-package) | `import_module("github.com/kurtosis-tech/geth-package/lib/geth.star")` |
| Reth | EL client | [Github](https://github.com/kurtosis-tech/reth-package) | `import_module("github.com/kurtosis-tech/reth-package/lib/reth.star")` |
| Lighthouse | CL client | [Github](https://github.com/kurtosis-tech/lighthouse-package) | `import_module("github.com/kurtosis-tech/lighthouse-package/lib/lighthouse.star")` |
| Mock-MEV | MEV Infra | [GitHub](https://github.com/kurtosis-tech/mev-package) | `import_module("github.com/kurtosis-tech/mev-package/lib/mev_launcher.star")` |
| Full MEV | MEV Infra | TBD | `TBD` |
| Nethermind | EL client | TBD | `TBD` |
| Erigon | EL client | TBD | `TBD` |
| Besu | EL client | TBD | `TBD` |
| Prysm | CL client | TBD | `TBD` |
| Teku | CL client | TBD | `TBD` |
| Nimbus | CL client | TBD | `TBD` |

### Composed Testnet Package Examples

| Package | URL | Import Statement |
| --- | --- | --- |
| Geth + Lighthouse | [Github](https://github.com/kurtosis-tech/geth-lighthouse-package) | `import_module("github.com/kurtosis-tech/geth-lighthouse-package/main.star")` |
| Reth + Lighthouse | [Github](https://github.com/kurtosis-tech/reth-lighthouse-package) | `import_module("github.com/kurtosis-tech/reth-lighthouse-package/main.star")` |
| Geth + Lighthouse + Mock-MEV Infra | [Github](https://github.com/kurtosis-tech/geth-lighthouse-mev-package) |  `import_module("github.com/kurtosis-tech/geth-lighthouse-mev-package/main.star")` |
| 2 EL clients + 2 CL clients + MEV Infra | TBD |  `TBD` |

### Roadmap

- [ ] Turn tables into pretty-formatted blocks so people can click-to-copy import statements
- [ ] Parameterize all composed testnet package examples
- [ ] Add README for quick start + install instructions to Kurtosis
- [ ] Fill out components marked "TBD"
- [ ] Fill out full MEV infra (rather than mock-mev)
- [ ] Find and include components for open-source explorers (beacon chain and execution layer)
