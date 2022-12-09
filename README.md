# Ethereum Light-Client State Proof

This repository contains Ethereum Light-Client State Proof project. In particular:

1. A program `state-proof-gen` that takes Ethereum's light-client state as an input and produces [Placeholder proof system-based](https://crypto3.nil.foundation/papers/placeholder.pdf) state proof. 
2. An in-EVM application logic `evm-proof-verify` that which verifies Ethereum's Light-Client state correctness.
3. A high-level description of the implemented proof system.

## Documentation

Project documentation, circuit definitions, API references etc can be found at https://github.com/nilfoundation/ethereum-state-proof/docs.

## State Proof Generator (`state-proof-gen`)

State proof generator is a zkLLVM-based C++ application using =nil; Crypto3 C++ Cryptography Suite (https://github.
com/nilfoundation/crypto3) for cryptographic primitives definition. It is supposed to be proven by =nil;'s [Proof 
Market](https://proof.market) provers. 

Such an application takes Ethereum's "beacon chain" data as an input and, after being processed by a 
[Proof Market](https://proof.market)'s participants, results into a [Placeholder proof system](https://crypto3.nil.
foundation/papers/placeholder.pdf)-based proof suitable for using within zkBridges, zkOracles or any other ways 
requiring "beacon chain"'s data.

### Dependencies

Libraries requirements are as follows:
* Boost (https://boost.org) (>= 1.76)

Compiler/environment requirements are as follows:
* CMake (https://cmake.org) (>= 3.13)
* GCC (>= 10.3) / Clang (>= 9.0.0) / AppleClang (>= 11.0.0)
* zkLLVM (https://github.com/nilfoundation/zkllvm)

## Community

Issue reports are preferred to be done with Github Issues in here: https://github.com/nilfoundation/ethereum-state-proof/issues.

Forum-alike discussion topics are better to be done with Discussions section in here: https://github.com/NilFoundation/ethereum-state-proof/discussions

Usage and development questions a preferred to be asked in Discord (https://discord.gg/KmTAEjbmM3) or a Telegram chat: https://t.me/nilfoundation