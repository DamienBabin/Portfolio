---
layout: default
title: Architecture Overview
nav_order: 2
parent: Important Concepts
grand_parent: Getting Started
permalink: /getting-started/important-concepts/2architecture/
---

# Architecture Overview

Our infrastructure follows a structured approach using Spacelift(should be applicable to TFC) to manage and deploy our Terraform code. This architecture enables scalability, maintainability, and proper separation of concerns.

## Repository Structure

Our infrastructure code is organized into three main components:

1. **Module Registry**: Contains reusable infrastructure components
   - Each module is version controlled
   - Modules are self-contained with clear inputs/outputs
   - Stored in separate repositories with semantic versioning

2. **Projects**: Complete infrastructure solutions
   - Combine modules to create full environments
   - Environment-specific configurations
   - Stored in separate repositories by business domain
   - Branch-based environment management:
     - `dev` branch for development
     - `qa` branch for quality assurance
     - `main` branch for production

3. **Workspace Management**: Orchestrates deployments
   - Manages stack creation and configuration
   - Handles environment separation (dev/qa/prod)
   - Controls access through policies
   - Manages dependencies between stacks
   - Configures branch-to-environment mapping:
     - Development stacks track `dev` branch
     - QA stacks track `qa` branch
     - Production stacks track `main` branch

## Stack Organization

Stacks in Spacelift are organized hierarchically:

1. **Environment Stack**
   - Foundation infrastructure (VPCs, networking, etc.)
   - Shared services and resources
   - Core security configurations
   - Required by all other stacks

2. **Business Unit Stacks**
   - Specific to each business domain
   - Built on top of environment stack
   - Isolated resources per business unit
   - Independent deployment cycles

## Dependency Management

Stack dependencies are managed through:

1. **Explicit Dependencies**
   - Environment stack as foundation
   - Clear parent/child relationships
   - Controlled deployment order

2. **Data Sharing**
   - Remote state access between stacks
   - Controlled through Spacelift policies
   - Explicit output/input relationships

## Environment Separation

Each environment (dev/qa/prod) is isolated through:

1. **Separate Stacks**
   - Individual stack per environment
   - Environment-specific variables
   - Controlled promotion between environments
   - Branch-based deployments
   - Promotion path: dev → qa → prod

2. **Access Control**
   - Environment-specific permissions
   - Role-based access control
   - Policy enforcement per environment

## Best Practices

Our architecture enforces several key principles:

1. **Modularity**
   - Reusable components
   - Clear separation of concerns
   - Version controlled modules

2. **Isolation**
   - Environment separation
   - Business unit isolation
   - Resource segregation

3. **Standardization**
   - Consistent naming conventions
   - Standard module interfaces
   - Common deployment patterns
   - Branch-based deployment strategy

4. **Security**
   - Least privilege access
   - Environment isolation
   - Controlled state access

This architecture provides a scalable and maintainable approach to infrastructure management while ensuring proper security and isolation between components.