---
description: Introduction to Trusted Platform Module (TPM)
---

# 1. Trusted Platform Module (TPM)

## What is a TPM?

The Trusted Platform Module (TPM) is a security tool that can be part of your computer's motherboard, CPU, or provided by a software that controls the system. It works below the level of the operating system and the boot sequence, which means it can check if these systems are safe even if they've been tampered with. TPMs are necessary for any device that is compatible with Windows, and they support features in Windows' BitLocker, ChromeOS, and Linux's Integrity Measurement Architecture.

However, if you look at the [many pages of guidelines and additional documents](https://trustedcomputinggroup.org/resource/tpm-library-specification/), you'll see that TPMs are quite complicated.

TPMs can check the boot state, identify devices, keep secrets, store complex key hierarchies, create complex authorization systems, and optionally secure/monitor/validate sessions. Its design is so versatile that in many situations, you could replace the term "TPM" with "magic security dust".

Here you should be able to run all examples there and it's a good option instead of getting new hardware. To keep things simple, we'll concentrate on TPM 2.0 on Linux, and we won't consider other operating systems and older versions.

### Comparision of the different TPM types

Interesting table is available at page 4 of this [TCG document](https://trustedcomputinggroup.org/wp-content/uploads/2019\_TCG\_TPM2\_BriefOverview\_DR02web.pdf)

**What does a TPM actually do?**

TPM is a physical component that’s usually built into your motherboard. Inside there are many components that let the TPM do its job. What is its job exactly? Here are the main tasks a TPM performs:

* The TPM stores passwords, security certificates, and encryption keys securely and prevents unauthorized tampering.
* It stores information about the computer securely, so it’s easy to detect if anyone has tampered with the computer.
* A TPM can securely generate encryption keys so that the process cannot be spied upon or interfered with.
