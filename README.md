# SecretVM: Confidential Virtual Machines 

This is the umbrella repository for the SecretVM project, a comprehensive platform for building, operating, and securing confidential virtual machines (CVMs) using Trusted Execution Environment (TEE) technologies.

## Project Components

| Repository | Description | Primary Function |
|------------|-------------|------------------|
| [secret-vm-build](https://github.com/scrtlabs/secret-vm-build) | Yocto-based build system for creating secure VM images | Building the foundational secure VM images |
| [secret-vm-ops](https://github.com/scrtlabs/secret-vm-ops) | Operational tools for VM management | Day-to-day operations of CVMs including startup and attestation |
| [secret-vm-kms](https://github.com/scrtlabs/secret-vm-kms) | Key Management System for secure key distribution | Managing cryptographic keys through attestation |
| [secret-vm-attest-rest-server](https://github.com/scrtlabs/secret-vm-attest-rest-server) | REST server for attestation reporting | Providing attestation services over HTTPS |
| [reproduce-mr](https://github.com/scrtlabs/reproduce-mr) | A CLI tool for calculating attestation measurements for SecretVM images | Indepentendly verifying the authenticity of SecretVM machines | 



## Component Details

### secret-vm-build

The SecretVM Build System creates reproducible, secure VM images that serve as the foundation for confidential computing environments.

**Key Features:**
- Creates reproducible VM images with attestation capabilities
- Builds both CPU-only and GPU-enabled configurations
- Produces trusted boot components (kernel, initramfs, UEFI firmware)
- Designed for production-grade security

### secret-vm-ops

This repository contains the operational tools required for running and managing SecretVMs.

**Key Features:**
- Secure VM startup scripts with attestation
- SSL certificate generation and management
- Cryptographic operations tooling
- Secure storage initialization and management

### secret-vm-kms

The Key Management System provides a framework for secure cryptographic key management through attestation-based validation.
The KMS is implemented as a Smart Contract running on Secret Network

**Key Features:**
- Service key management with attestation-based access control
- Image-specific secret key distribution
- Environment secret management

### secret-vm-attest-rest-server

A lightweight REST server that provides attestation reports for confidential VMs over HTTPS.

**Key Features:**
- Multiple attestation endpoints (GPU, CPU, self)
- Secure communication with TLS
- Visualization of attestation data
- Docker integration for container monitoring

## Use Cases

- **Confidential AI**: Privacy-preserving machine learning workloads
- **AI Agents**: Verifible AI agents
- **MCP Servers**: Model-Context Protocol server, exposing additional capabilities to LLMs
- **Secure Blockchain Operations**: Protection for sensitive blockchain operations
- **Regulated Data Processing**: Compliant processing of sensitive data
- **Multi-party Computation**: Secure collaboration on sensitive data

### reproduce-mr
A command-line tool that emulates the calculation of attesation registers (MRTD, RTMR0, RTMR1, RTMR2, RTMR3)

**Key Features:**
- Calculates the expected values of all attestation registers based on given VM artifacts, docker-compose.yaml and other parameters
- Used to verify the chain of trust, ensuring that a given SecretVM is indeed built from given artifacts

