

# [Designing G-Coin](https://gtv1.org/)

# 1. What is G-Coin?

A unique cryto-currency powered by blockchain technology and accepted by all G-Media platforms (e.g., G-Fashion / G-Club) and all over the world.

## Objectives

- Rewarding system to encourage news integrity
- G-Coin payment for G-Fashion / G-Club
- Global currency and settlement (realization) ideally with Gold Reserve anchored with Gold
- Blockchain / cryto-currency
- Decentralized / Security Committee for regulation
- Trust / Investment Committee lessons learned from BAT due to injustice and corruption
- Stablized not like Ponzi Scheme or BitCoin Scheme

## Principles

- talent No.1
- rule of law
- truth and justice back by power

# 2. Requirements and Goals of the System

## Functional Requirements:

- Voting for Association to issue new coins, centralization/Fed?
- Producing on G-TV top-up or rewarded from others
- Consuming on G-Fashsion / G-Club
- Payment, transaction correctness regardless content => security

## Non-Functional Requirements:

- The system should be highly available.
- low latency. 200ms per transaction but could be longer depending on network
- Consistency - eventual consistent is acceptable across various devices
- highly reliable, no lost coins
- scalability
- security
- usability

## Some Design Considerations

- refer to Bitcoin or [Ethereum](https://en.wikipedia.org/wiki/Ethereum)
- Turing-incomplete (Bitcoin) simpler but heavily depending on computing power to ensure security
- Turing-complete (Ethereum) security

# 3. Capacity Estimation and Constraints

- Let's assume we have 2B total users, with 1B daily active users globally
- Average transaction per day => 1B

## Traffic estimates:

## Storage estimates:

## Bandwidth estimates:

## Memory estimates:

## High level estimates:

# 4. System APIs

## Parameters:

## Returns:

## How do we detect and prevent abuse?

# 5. High Level System Design


# 6. Database Design

## Database Schema:

## What kind of database should we use?

Using MySQL but need to address problem like **Latency and consistency in High Availability MySQL in distributed system across multi data centers globally** which requires understanding of CAP Theorem and Paxos Algorithm

## CAP Theorem and Paxos Algorithm

- Databases may only excel at two of the following three attributes: consistency, availability and partition tolerance
- Relational databases tend to excel at consistency and partition tolerance
- NoSQL tend to excel at availability and partition tolerance

> https://github.com/libra/libra/blob/testnet/consensus/README.md

# 7. Data Size Estimation

# 8. Component Design

# 9. Reliability and Redundancy

# 10. Data Partitioning and Replication (Sharding)

## a. Range Based Partitioning

## b. Hash-Based Partitioning

## [Consistent Hashing](https://www.toptal.com/big-data/consistent-hashing)

# 11. Ranking and GTV Feed Generation

# 12. GTV Feed Creation with Sharded Data

# 13. Cache

**How much cache memory should we have?**
**Which cache eviction policy would best fit our needs?**
**How can each cache replica be updated?**

# 14. Load Balancer (LB)

We can add a Load balancing layer at three places in our system:

- Between Clients and Application servers
- Between Application Servers and database servers
- Between Application Servers and Cache servers


# 15. Purging or DB cleanup

# 16. Telemetry

# 17. Security and Permissions

