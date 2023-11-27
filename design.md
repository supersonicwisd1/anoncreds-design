# Design Document: Extending ACA-Py for W3C VC/VP Support

## Introduction

This design document proposes an extension to the Aries Cloud Agent Python (ACA-Py) to enable support for Hyperledger AnonCreds credentials and presentations in the W3C Verifiable Credentials/Verifiable Presentations (VC/VP) format. This will lead to the removal of the "lagacy" format and introduction the use of W3C format of data model

## Objectives 

- An issuer issuing a W3C VC Format AnonCreds credential.
- An issuer issuing a W3C VC Format credential with both an AnonCreds and another signature, such as from the generation of a Data Integrity Proof using an Ed25519 key.
- This idea of a credential with multiple different types of signatures (working name “FlexCreds”) is a form of “cryptographic agility”, enabling a single credential to be used in different verifier use cases driven by different signature requirements.
- An Aries Cloud Agent Python holder receives a W3C VC Format AnonCreds credential from an issuer and stores it.
- On request for a presentation from a verifier, an Aries Cloud Agent Python holder retrieves stored W3C VC Format AnonCreds credentials and assembles in W3C VP Format an AnonCreds presentation and sends it to the verifier.
- An Aries Cloud Agent Python verifier receiving a W3C VP Format AnonCreds presentation verifies the presentation.

