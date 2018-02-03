# Token-Based Federation

## Abstract

Token-Based Federation (TBF) is an OAuth 2.0 federated authorization framework.
TBF defines interfaces, flows and constructs for coordinating access to heterogeneous OAuth 2.0
resource servers across multiple administrative domains.

## Introduction

To begin with, there are two different definitions for the term federation:

1. Information exchanging between heterogeneous networks (telecommunications networks)  
2. Collective authority (federated identity)

The TBF framework refers to the No. 1 definition.

##Architectural Principle

The OAuth 2.0 authorization framework was originally designed for B2C scenarios. In OAuth the roles of the Resource Owner (RO), Authorization Server (AS), Resource Server (RS) and Client are co-located, they are all under the realm of a single trust domain.
The TBF framework defines two new roles: Sender and Recipient, both under its own trust domain.
The Sender role acts as RO and Recipient is a complete new role. 
The AS, Client and RS roles are dislocated between Sender's and Recipient's trust domain.
The Client is under the realm of the Sender's trust domain, and RS is under the realm of the Recipient's trust domain. There are no cross-domain Sender's Client/Recipient's AS and Recipient's RS/Sender's AS contracts.
The Client is registered only once with the Senders' AS and the Recipient's RS is registered only once with the Recipient's AS.
There is a trust between Sender's AS and Recipient's AS.
The TBF mechanism is handled by the cross-domain autonomic control loop through two authorization servers each in its own administrative domain.

## OSI Model from TBF perspective

[OSI Model]

## Federated Trust Relationship

Each Federated Trust Relationship between two administrative domains is defined as
an asymmetric one-way trust between Trustor and Trustee paired with the reflexive asymmetric
unidirectional federation between Sender and Recipient.

[Understanding OAuth 2.0 access, trust and federation directions] 

## Low-Level Use Cases

### Authentication and Authorization

* Identity and Attribute Providers
* User-Managed Access

## Medium-Level Use Cases

### Public Key Infrastructure

* [Identity-Based Privacy]
* [Encryption Key Generator]

### Signaling

* VoIP
* WebRTC

### Task Delegation

* Workflow System

### Blockchain

* Federated Ledger

## High-Level Use Cases

### New FTP/email-like services

* File Transfer System
* Content Transfer System
* Persistent Group Chat

[OSI Model]: https://github.com/token-7/token7-specs/wiki/OSI-Model-from-TBF-perspective
[Understanding OAuth 2.0 access, trust and federation directions]:  https://github.com/token-7/token7-specs/wiki/Understanding-OAuth-2.0-access,-trust-and-federation-directions
[Identity-Based Privacy]: https://igi64.github.io/ibp.html
[Encryption Key Generator]: https://igi64.github.io/airykey.html
