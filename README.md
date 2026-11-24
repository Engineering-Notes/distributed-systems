# Engineering Notes: Distributed Systems

[![CI](https://github.com/Engineering-Notes/distributed-systems/actions/workflows/ci.yml/badge.svg)](https://github.com/Engineering-Notes/distributed-systems/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Node.js 22](https://img.shields.io/badge/node-22-339933.svg)](.nvmrc)

Clocks, consensus, quorums, replication and failure, measured.

Tested code behind the **Distributed Systems** series of [Engineering Notes](https://github.com/Engineering-Notes), published on [codemwangi.substack.com](https://codemwangi.substack.com). The series starts on Tuesday 19 January 2027. Every number quoted in an article will come from the code in its folder, and CI runs all of it on every change.

## Articles

| No. | Article | Code | Publishes |
|---|---|---|---|
| 01 | Clocks: wall time, monotonic time and logical clocks, measured under skew | coming | 19 Jan 2027 |
| 02 | Vector clocks and hybrid logical clocks | coming | 20 Jan 2027 |
| 03 | Raft leader election under network partitions | coming | 21 Jan 2027 |
| 04 | Raft log replication and stale leaders | coming | 26 Jan 2027 |
| 05 | Quorums: N, R and W, and how stale reads happen | coming | 27 Jan 2027 |
| 06 | CRDTs against last-write-wins | coming | 28 Jan 2027 |
| 07 | Consistent hashing, rendezvous and jump hash | coming | 2 Feb 2027 |
| 08 | Failure detection: heartbeats, phi accrual and SWIM | coming | 3 Feb 2027 |
| 09 | Ordering and delivery in a partitioned log | coming | 4 Feb 2027 |
| 10 | Backpressure, queueing and load shedding | coming | 9 Feb 2027 |
| 11 | Caching: stampedes, invalidation and consistency | coming | 10 Feb 2027 |
| 12 | Sagas against two-phase commit | coming | 11 Feb 2027 |
| 13 | Checking linearizability with a small Jepsen-style checker | coming | 16 Feb 2027 |
| 14 | Capstone: a replicated key-value store under partitions | coming | 17 Feb 2027 |

## Running an article

Each article lives in its own folder, `NN-name`, with its own `package.json`, lockfile and tests.

```bash
git clone https://github.com/Engineering-Notes/distributed-systems.git
cd distributed-systems
docker compose up -d        # PostgreSQL 16, for the articles that need it
cd 01-<name>
npm ci
npm test
```

`npm test` exits with an error if the approach an article recommends ever produces a wrong result.

## Related

- [Payment Systems](https://github.com/Engineering-Notes/payment-systems), the first series.
- [Contributing](https://github.com/Engineering-Notes/.github/blob/main/CONTRIBUTING.md), [code of conduct](https://github.com/Engineering-Notes/.github/blob/main/CODE_OF_CONDUCT.md) and [security policy](https://github.com/Engineering-Notes/.github/blob/main/SECURITY.md) apply to this repository.

## Licence

[MIT](LICENSE)
