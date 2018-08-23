# Spring 2018 Documentation Research

In spring 2018, Protocol Labs did extensive research into the IPFS onboarding process and related documentation. The specific goals of this research were to understand where people get stuck in their understanding of IPFS, what existing resources are helpful, and where our existing learning are failing develoers using IPFS (whether they are new to it or not).

* [Full IPFS Documentation Research Review](https://ipfs.io/ipfs/QmNj68gTzAs9QbfMKzMGurXP2WCmA6GTcKuUkWm4kBV1Qn/html/)
* [Summary and review of GitHub repos](https://docs.google.com/spreadsheets/d/1IDVAGfniyHCJLIxLc3y7K7YTOFGCtgwTVCZEojtNLlw)
* [Summary and review of all discussion board posts (as of mid-March)](https://docs.google.com/spreadsheets/d/1Z0Wy_jSS-42gXP9n1MA9JifZ7PDvNEVbpbfTFTVlz8M)
* [Roadmap for work based this research in GitHub](https://github.com/ipfs/docs/issues/58)
* Ongoing documentation work in the [ipfs/docs](https://github.com/ipfs/docs) repo. (The issues are also used for managing documentation improvements across various IPFS projects and are not limited to just the new docs site).


## Summary

1. There is **no clear introduction** to the overall idea of exactly how IPFS works and what it’s doing. (Most people still recommend the whitepaper, even if it’s old and no longer fully accurate; it also looks really academic and can be intimidating.) (See ipfs/docs#60)
2. IPFS has **lots of new concepts** (whether you are knowledgeable about things like graphs or not) that are just very different from the web technologies people know today. (See ipfs/docs#56)
3. **Docs are inconsistently located** and spread across a number of repos people have to hunt through. (See ipfs/docs#68)
4. **Clear, standard API docs** are not always available.
5. **Hunting through GitHub is hard.** (Which repos have docs? Where in the repo are they? Which projects are important and how do they relate to the others? Which repos and docs are up-to-date?) (See ipfs/docs#54, ipfs/docs#57)


## Top discuss.ipfs.io Topics

| Tag        | Count |      |
| ---------: | ----: | :--- |
| troubleshooting | 66 | ////////////////////////////////////////////////////////////////// |
| basics | 46 | ////////////////////////////////////////////// |
| ipns | 32 | //////////////////////////////// |
| use-cases | 31 | /////////////////////////////// |
| explanation | 22 | ////////////////////// |
| api | 20 | //////////////////// |
| features | 20 | //////////////////// |
| announcement | 20 | //////////////////// |
| go-ipfs | 18 | ////////////////// |
| tools | 17 | ///////////////// |
| cli | 17 | ///////////////// |
| js-ipfs | 16 | //////////////// |
| status | 15 | /////////////// |
| concepts | 15 | /////////////// |
| privacy | 12 | //////////// |
| networking | 11 | /////////// |
| dynamic-data | 11 | /////////// |
| ideas | 11 | /////////// |
| pinning | 11 | /////////// |
| performance | 10 | ////////// |
| filecoin | 10 | ////////// |
| security | 9 | ///////// |
| files | 9 | ///////// |
| community | 8 | //////// |
| uploading | 8 | //////// |
| cluster | 8 | //////// |
| bug | 8 | //////// |
| gateway | 7 | /////// |
| windows | 7 | /////// |
| private-networks | 7 | /////// |
| pubsub | 7 | /////// |

This is based on an inventory of discuss topics as of 2018-03-05, which you can find in this Google Sheet: https://docs.google.com/spreadsheets/d/1Z0Wy_jSS-42gXP9n1MA9JifZ7PDvNEVbpbfTFTVlz8M Tags are a combination of those assigned by the topic author on the discuss site and manual tags we’ve applied to the inventory to get more detail.


## Concepts & Terms that Trip People Up

- DWeb
- DHT
- Content Routing/p2p Routing
- Graph
- DAG
- Merkle Tree/DAG
- Merkle “Forest”
- Hash
- Gateway
- Pinning
- Transport
- Swarm
- Information Space
- MFS
- (Cryptographic) Signing
- Peer
- Peer ID
- CRDT
- Repo
- DataStore
- Node, Daemon
- CID (v0, v1, …)
- Path/Address
- DNSLink
- CBOR
- Bitswap
- Blocks
- Bootstrap Node
- Listening
- Dialing
- Announcing
- Relay
- GC/Garbage Collection


## GitHub/Source-Related Issues

**Organization:**

- Inventory of GitHub repositories as of 2018-03-15: https://docs.google.com/spreadsheets/d/1IDVAGfniyHCJLIxLc3y7K7YTOFGCtgwTVCZEojtNLlw This has one tab for each org (ipfs, ipld, libp2p, multiformats, ipfs-shipyard), but only the `ipfs` is fully annotated:

    - Gray lines are deprecated repos.
    - Orange lines are repos of unknown status (can't tell if they are active, kinda sleepy, deprecated, intended to be moved, etc.) We might know the status of some (but surprisingly not all!), but community members and people new to IPFS definitely don’t.
    - Red lines are repos with significant problems. Usually this means either they lack a license (and so are not open source) or they are deprecated but not marked in any way as such (someone could easily waste a lot of time trying to use them before realizing they are a dead end).
    - Green is organizing/discussion, blue is docs/specs.
    - For a full key, see the “key” tab.

- There are *lots* of repos, but a huge number of them are deprecated. Not all the deprecated ones are marked as such, which adds more confusion. Archiving these repos can help reduce noise (they don’t show up in most views), but at least making sure they are consistently marked as deprecated (and in a consistent *way*) can at least reduce confusion.

- Empty READMEs and repo description lines: both of these are important cues for people to understand what a repo is and what it’s for, but are often empty. Additionally, some READMEs are empty in value even though they appear structured and have text — it looks like there was a push to validate READMEs with `standard-readme` at some point, and people reacted by filling in the required structure with “TODO” or placeholder content, which defeats the point of having the check and makes it easy for the READMEs to continue to fail in their purpose.

- Naming conventions are often inconsistent. Sometimes there’s even more than one attempt at a convention for a given type of thing (e.g. `*-ds-*` vs. `*-store-*` for datastore implementations). This is a tough one to fix (renaming a project is all kinds of messy).

**Licensing:** for the most part, this is good, but:

- **Some repos are unlicensed** or only refer to their license by name (e.g. “MIT”) without the actual license text or a link in the readme or source, which is effectively unlicensed. These repos are not actually open-source in any legal sense.

- **Discussion/organizing repos have inconsistent licensing.** It seems like, at some point, there was a push to make them Creative Commons-licensed (which seems more reasonable for discussion than MIT), but there are quite a few that are MIT licensed instead.

**Contributing:**

- Contribution Instructions: There are two standard styles of listing contribution instructions:
    - Animated gif + link: https://github.com/ipfs/go-ipfs#contributing
    - Minimal text + link to `standard-readme` spec: https://github.com/ipfs/ipfs-cluster#contribute
    - Plus some repos don't fit any convention (or just don’t have instructions)

- Contributors: most (but not all) `js-*` repos list contributors in `package.json`. NO other projects list contributors anywhere, but instead rely on Git/GitHub metadata. (Worth noting: this misses out on contributions that do not show up as *Git commits*)
