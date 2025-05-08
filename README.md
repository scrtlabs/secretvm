# SecretVM: Confidential Virtual Machines

This is the umbrella repository for the SecretVM project, a comprehensive platform for building, operating, and securing confidential virtual machines (CVMs) using Trusted Execution Environment (TEE) technologies.

## Project Components

| Repository | Description | Primary Function |
|------------|-------------|------------------|
| [secret-vm-build](https://github.com/scrtlabs/secret-vm-build) | Yocto-based build system for creating secure VM images | Building the foundational secure VM images |
| [secret-vm-ops](https://github.com/scrtlabs/secret-vm-ops) | Operational tools for VM management | Day-to-day operations of CVMs including startup and attestation |
| [secret-vm-kms](https://github.com/scrtlabs/secret-vm-kms) | Key Management System for secure key distribution | Managing cryptographic keys through attestation |
| [secret-vm-attest-rest-server](https://github.com/scrtlabs/secret-vm-attest-rest-server) | REST server for attestation reporting | Providing attestation services over HTTPS |

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

**Key Features:**
- Service key management with attestation-based access control
- Image-specific secret key distribution
- Environment secret management
- Cryptographic operations with ephemeral keys

### secret-vm-attest-rest-server

A lightweight REST server that provides attestation reports for confidential VMs over HTTPS.

**Key Features:**
- Multiple attestation endpoints (GPU, CPU, self)
- Secure communication with TLS
- Visualization of attestation data
- Docker integration for container monitoring

## Getting Started

Please refer to the individual component repositories for specific setup and usage instructions.

For a complete SecretVM deployment, you'll typically need to:

1. Build VM images using secret-vm-build
2. Set up operational tools using secret-vm-ops
3. Deploy the attestation server from secret-vm-attest-rest-server
4. Configure key management using secret-vm-kms

## Use Cases

- **Confidential AI**: Privacy-preserving machine learning workloads
- **Secure Blockchain Operations**: Protection for sensitive blockchain operations
- **Regulated Data Processing**: Compliant processing of sensitive data
- **Multi-party Computation**: Secure collaboration on sensitive data

## License

All SecretVM components are licensed under the Apache License 2.0.
