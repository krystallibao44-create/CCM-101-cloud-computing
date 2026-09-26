# Laboratory Activity 5: The Cloud Data Engineer

Mission Objective: Deploy an S3-compatible, high-performance object storage server using MinIO on Docker, establish secure web console access, and manage unstructured media assets for a scalable application.

## Mission Overview

As part of the Cloud Data Engineering Team at CloudNova Technologies, this proof-of-concept tackles a common pain point: container storage is temporary by nature, so a web app has no safe way to keep persistent media files inside its own ephemeral web server container. This activity sets up a separate, production-ready object storage backend built specifically to host unstructured media assets.

## Objectives & Key Deliverables

- Architectural Research: Compare Block, File, and Object Storage mechanisms.
- Container Deployment: Launch an S3-compatible MinIO server via Docker with environmental parameters.
- Network Routing: Map and route administrative web traffic through port forwarding.
- Data Operations: Provision storage buckets (`client-photos`) and upload media objects.
- Documentation: Compile technical implementation details and reflective analysis.

## Stack & Infrastructure

| Layer | Component | Description |
| :--- | :--- | :--- |
| **Containerization** | Docker Engine | Lightweight container runtime |
| **Storage Engine** | MinIO | S3-Compatible Object Storage Server |
| **Host Environment** | Linux (Ubuntu) | KillerCoda Cloud Playground |
| **Console Access** | Port 9001 | Web GUI Management Interface |
| **API Endpoint** | Port 9000 | Programmatic S3 API Interoperability |

## Key Skills Mastered

- Docker Management: Container lifecycle control, custom port mappings (`-p`), and environment variable injection (`-e`).
- Cloud Storage Provisioning: Bucket administration, access control setup, and object management.
- Technical Documentation: Writing structured, production-ready Markdown documentation for cloud workflows.
