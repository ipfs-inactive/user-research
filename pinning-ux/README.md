# 2019 Q4 endevour: pinning ux

📌  
📌Please follow along or contribute to this work via [issues tagged `[Area] Pinning UX`](https://github.com/ipfs/user-research/issues?q=is%3Aissue+is%3Aopen+label%3A%22%5BArea%5D+Pinning+UX%22).  
📌You can also spelunk in this repo's [`pinning-ux` directory](/pinning-ux).   
📌  

## Problem statement

A growing challenge for IPFS is to define the product story for how users interact with and think about [pins](https://docs.ipfs.io/guides/concepts/pinning/) in IPFS. As the number of types of pins increases (for example, pinning [selectors](https://github.com/ipld/specs/blob/master/selectors/selectors.md)), and properties such as [ipfs-desktop](https://github.com/ipfs-shipyard/ipfs-desktop/) and soon [ipfs-cluster](https://cluster.ipfs.io/) add new entry points for visualizing and managing pins, we need a holistic product story that will unify the communication and visualization of pinsets and their potential interactions in a way users understand. For example:

- What are common user journeys for configuring and interacting with pins in IPFS?
- How should we introduce and communicate different types of pins (direct vs indirect vs recursive) in IPFS across various types of interfaces?
- What is the consistent set of abstractions and visual language for managing and configuring different pin types? 
- How should people reason about their ipfs pinset and the human actions they want to take on that pinset?
- How should various ipfs entry points - the [ipfs CLI](https://docs.ipfs.io/reference/api/cli/#ipfs-pin), [webUI](https://github.com/ipfs-shipyard/ipfs-webui/), [ipfs-companion](https://github.com/ipfs-shipyard/ipfs-companion#ipfs-companion), [ipfs-cluster](https://cluster.ipfs.io/), 3rd party pinning services such as [Pinata](https://pinata.cloud/), [Infura](https://infura.io/), [Eternum](https://www.eternum.io/), etc - visualize and allow configuration of your pins?


**Objective**
+ Define how users should represent, interact with, and reason about their pins in IPFS across entry points

**Key Results**
1. Identify the top pinning user journeys for each ipfs entrypoint
1. Define and prioritize the portfolio of pinning features and flows to surface in each entry point
1. Create a consistent visual / verbal way of representing these features and states in a way that makes sense to ipfs users in each context
