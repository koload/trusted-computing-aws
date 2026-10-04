This repository contains the practical Proof of Concept (PoC) for a master's thesis on trusted digital evidence processing in distributed cloud environments. The project aims to eliminate the need for physical trust in cloud operators by implementing a Zero Trust architecture.

The system relies on three core pillars:

* **Control Plane:** A containerized Django application deployed on AWS ECS that orchestrates the flow of evidence and verifies business logic.
* **Isolated Processing:** AWS Nitro Enclaves provide a hardware-isolated compute space to decrypt, verify, and cryptographically hash sensitive evidence.
* **Immutable Storage:** Amazon S3 with Object Lock acts as the final archive, preventing the deletion or modification of the cryptographic proofs to guarantee non-repudiation.

The underlying cloud infrastructure is provisioned entirely as Infrastructure as Code (IaC) using Terraform, while GitHub Actions handle the automated CI/CD deployment. Extensive code comments are maintained throughout the entire codebase, serving as the primary documentation for all architectural decisions and system logic.
