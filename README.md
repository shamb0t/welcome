# Welcome to OrbitDB!

[![](https://img.shields.io/badge/project-orbit-red.svg?style=flat-square)](https://github.com/orbitdb/orbitdb)
[![](https://img.shields.io/badge/freenode-%23orbitdb-blue.svg?style=flat-square)](https://webchat.freenode.net/?channels=%23orbitdb)

> The main repository for discussing orbit

[`orbit-db`](https://github.com/haadcode/orbit-db) is a serverless, distributed, peer-to-peer database. `orbit-db` uses [IPFS](https://ipfs.io/) as its data storage and [IPFS Pubsub](https://github.com/ipfs/go-ipfs/blob/master/core/commands/pubsub.go#L23) to automatically sync databases with peers. It's an eventually consistent database that uses [CRDTs](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type) for conflict-free database merges making `orbit-db` an excellent choice for offline-first applications.

This organization is a place to bring together all fo the Orbit repositories, and to work together on making orbit better. This repo is the center of that organization.

## Repositories

The [@orbitdb](https://github.com/orbitdb) organization on GitHub contains many different repositories. For the most part, these fall into three categories: code which relates to OrbitDB, the peer to peer database for the decentralized web; Orbit Chat, a decentralized chat program built using OrbitDB; and various non-code repositories. Those three repositories are:

- The **[welcome](https://github.com/orbitdb/welcome)** community repo, which you're in right now;
- **[awesome-orbitdb](https://github.com/orbitdb/awesome-orbitdb)**, which is an attempt to list everything that is using OrbitDB, or could help people. Basically, what has been built? And;
- **[research](https://github.com/orbitdb/research)**, where you can find research papers and interesting research work on CRDTs and the like.


### OrbitDB

OrbitDB is a peer-to-peer database for the decentralized web (to put it succinctly). The most important repositories are:

- **[orbit-db](https://github.com/orbitdb/orbit-db)** - The main repo for OrbitDB.
- **[ipfs-log](https://github.com/orbitdb/ipfs-log)** -  The most important module used by OrbitDB.


And then, there are a whole host of helper modules. It should be noted that **all** of these are JavaScript modules on npm.

- **[crdts](https://github.com/orbitdb/crdts)** - A library of [Conflict-Free Replicated Data Types](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type) for JavaScript. Used in [orbit-db-counterstore](https://github.com/orbitdb/orbit-db-counterstore); mostly just one function is used.
- **[orbit-db-cache](https://github.com/orbitdb/orbit-db-cache)** - Actually a persistency layer, not a cache. Saves the latest HEAD of each db locally into LevelDB. Doesn't store a huge amount of data, just the amount of DBs you have. For all of the dbs you have locally, you have a hash for each.
- **[orbit-db-cli](https://github.com/orbitdb/orbit-db-cli)** - CLI for OrbitDB.
- **[orbit-db-counterstore](https://github.com/orbitdb/orbit-db-counterstore)** - Datastore in OrbitDB. Uses CRDTs, inherits from [orbit-db-store](https://github.com/orbitdb/orbit-db-store).
- **[orbit-db-docstore](https://github.com/orbitdb/orbit-db-docstore)** - Another OrbitDB store which allows you to index a blob.
- **[orbit-db-eventstore](https://github.com/orbitdb/orbit-db-eventstore)** - Another data model type. Like [ipfs-log](https://github.com/orbitdb/ipfs-log). Wraps into a store interface.
- **[orbit-db-feedstore](https://github.com/orbitdb/orbit-db-feedstore)** - Database type in OrbitDB. This is exactly like eventlog, but you can delete events from the log.
- **[orbit-db-keystore](https://github.com/orbitdb/orbit-db-keystore)** - Keystore is actually a module that stores the keys locally. You can generate keys, it persists them in the data folder, you can import and export keys - it is basically a key manager.
- **[orbit-db-kvstore](https://github.com/orbitdb/orbit-db-kvstore)** - KeyValue store. Another DB type in OrbitDB. This may occasionally be unclear in the code, where `kvstore` is called `keyvalue` store.
- **[orbit-db-pubsub](https://github.com/orbitdb/orbit-db-pubsub)** - Message propagation module for OrbitDB. A layer between OrbitDB and IPFS Pubsub.
- **[orbit-db-store](https://github.com/orbitdb/orbit-db-store)** - Base class for OrbitDB data stores. A Base Class defines the common interface for all databases.


### Orbit Chat

And then there is the Orbit Chat, which is a chat program built on top of OrbitDB. These will most likely be renamed at some point to stop the confusion. The most important repository is:

- **[orbit-web](https://github.com/orbitdb/orbit-web)** - The browser client of Orbit Chat.

Other repositories include:

- **[orbit](https://github.com/orbitdb/orbit)** - This is a landing page repo, without code, and may be the start for a new Orbit Chat org if we end up making one. It needs to be updated.
- **[orbit-core](https://github.com/orbitdb/orbit-core)** - 
The JavaScript npm module that implements the Orbit Chat protocol.
- **[orbit-electron](https://github.com/orbitdb/orbit-electron)** - Desktop application for Orbit Chat. Uses orbit-core and IPFS.
- **[orbit-textui](https://github.com/orbitdb/orbit-textui)** - A terminal client for Orbit Chat.
- **[orbit-bot](https://github.com/orbitdb/orbit-bot)** - Unsurprisingly, a bot for Orbit Chat.

### Other repositories?

There are other repositories that aren't in the organization around the web which are important - for instance, of course, [ipfs](https://github.com/ipfs/ipfs). For now, these are the main ones in the @orbitdb organization.

If there is something missing form this list, please let us know! Either open a PR or an issue, and we'll add it. Thank you.


### Naming

Why "OrbitDB"? Because it was available on GitHub, and it matches [`orbitdb`](https://github.com/orbitdb/orbit-db). Why "Orbit"? Because that is the name of [the chat app built on top of orbit-db](https://github.com/orbitdb/orbit). Why was that called "Orbit"? You'll have to ask [@haadcode](https://github.com/haadcode), but it's probably something to do with the [InterPlanetary File System (IPFS)](https://github.com/ipfs/ipfs).

There are variants of the name. For now, the canonical versions are: OrbitDB for the general project, `orbit-db` for the codebase at `orbitdb/orbit-db`, `@orbitdb` for the organization, and Orbit Chat for what used to be called just Orbit.

## Contribute

Please contribute! [Dive into the issues](https://github.com/orbitdb/orbitdb/issues)!

Check out our [contributing document](contributing.md) for more information on how we work, and about contributing in general. Please be aware that all interactions related to OrbitDB are subject to the OrbitDB [Code of Conduct](https://github.com/ipfs/community/blob/master/code-of-conduct.md).

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

This repository is maintained by [@RichardLitt](https://github.com/RichardLitt). If you've got any questions for him, feel free to open an issue or a pull request, or to [email him](mailto:richardlitt@orbitdb.org) privately. we're always looking for more maintainers!

## License

This repository is only for documents. All of these are licensed under the [CC-BY-SA 3.0](LICENSE) license © 2016-2018 Protocol Labs Inc., Haja Networks Oy. Any code is under a [MIT](LICENSE) © 2016-2018 Protocol Labs Inc., Haja Networks Oy.
