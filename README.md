# eth-kurtosis

An index of packages and examples for getting started with building full-featured, private Ethereum testnets using full staking Ethereum nodes and support for all 10 major EL and CL client implementations. Kurtosis is used as a tool under the hood to create reproducible and modular environment definitions. 

### Why private testnets?
Private testnets are critical for developers working on the protocol, as well as smart contract developers who want to run their own chain using their own initial state for more complex applications. 
* For protocol developers, private testnets provide for an isolated life-like environment where they can safely prototype and validate network-level changes before mainnet forks, like the Merge, Shapella, and Dencun ([EIP-4844](https://www.eip4844.com/)). Private testnets have the added benefit of enabling the testing of behaviors against multiple client implementations as part of the effort to improve Ethereum's resilience via [client diversity](https://clientdiversity.org/). 
* For dApp developers, private testnets offer a foundation for validating the functionality of their applications that involve multiple chains (e.g. bridges, L2s, IBC protocols, etc)  or middle ware infrastructure (e.g. oracles, relayers, DVT nodes, etc).   

### Why use Kurtosis?
[Kurtosis](https://www.kurtosis.com/) is an open-source tool for defining and building private testnets. Testnet definitions built using Kurtosis are:
* Composable - import & build your testnet the way you want, including any combination of the various client types or any  other services that you would need for your testnet like databases, indexers, explorers, oracles, relayers, etc.
* Entirely reproducible - will work the same way on your laptop, in CI, or in the cloud.  
* Portable - works on both Docker and Kubernetes
* Scalable - testnet size can be any size you desire - only limited by underlying hardware
* Easy to write - the DSL used is called Starlark, a dialect of Python. Say goodbye to `yaml`.
* [Alpha & optional] Fully managed - write your environment definition once & deploy it to the cloud with a single click. Sign up for early access [here](https://mp2k8nqxxgj.typeform.com/to/U1HcXT1H?typeform-source=github.com).

To see an example of a full-featured, Ethereum private testnet definition currently in use by the Ethereum Foundation, check out the [`eth-network-package`](https://github.com/kurtosis-tech/eth-network-package).

### Available Testnet Components

| Component | Type | URL | Import Statement |
| --- | --- | --- | --- |
| Geth | EL client | [Github](https://github.com/kurtosis-tech/geth-package) | `import_module("github.com/kurtosis-tech/geth-package/lib/geth.star")` |
| Reth | EL client | [Github](https://github.com/kurtosis-tech/reth-package) | `import_module("github.com/kurtosis-tech/reth-package/lib/reth.star")` |
| Lighthouse | CL client | [Github](https://github.com/kurtosis-tech/lighthouse-package) | `import_module("github.com/kurtosis-tech/lighthouse-package/lib/lighthouse.star")` |
| Mock-MEV | MEV Infra | [GitHub](https://github.com/kurtosis-tech/mev-package) | `import_module("github.com/kurtosis-tech/mev-package/lib/mev_launcher.star")` |
| Full MEV | MEV Infra | TBD | `TBD` |
| Nethermind | EL client | [GitHub](https://github.com/kurtosis-tech/nethermind-package) | `import_module("https://github.com/kurtosis-tech/nethermind-package/lib/nethermind.star")` |
| Erigon | EL client | [Github](https://github.com/kurtosis-tech/erigon-package) | `import_module("https://github.com/kurtosis-tech/erigon-package/lib/erigon.star")` |
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
- [ ] Find and include high-value middleware infrastructure to include (oracles, relayers, DVT nodes)
- [ ] Add the web3-tools packages & examples for contract deployment to the private testnets
- [ ] Add "shadow forking" as a native package for use in private testnets for forking mainnet data
- [ ] Add middleware infrastructure packages like Hyperlane relayers, oracles, L2 nodes, SSV nodes, etc
