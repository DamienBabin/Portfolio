---
layout: default
title: Modules and Projects
nav_order: 1
parent: Important Concepts
grand_parent: Getting Started
permalink: /getting-started/important-concepts/1modules-projects/
---

# Modules and Projects

In Infrastructure as Code (IaC), organization is key to maintaining scalable and manageable systems. Think of building infrastructure like constructing buildings - you need both basic building materials (modules) and blueprints for complete structures (projects).

## The Construction Analogy

Imagine building with LEGO® bricks:
- **Modules** are like the individual LEGO® bricks - standardized, reusable pieces that serve specific purposes
- **Projects** are like the instruction manuals for complete LEGO® sets - they define how to combine those bricks into a functional structure

## Modules (The Bricks)

A **module** is a reusable, self-contained unit of infrastructure code that performs a specific task or creates a specific resource. Like standardized bricks, modules are:

- **Reusable**: Can be used in multiple projects
- **Self-contained**: Have clear inputs (variables) and outputs
- **Single-purpose**: Focus on one specific infrastructure component
- **Versioned**: Stored in a registry for consistent use

### When to Create a Module

Create a module when you have infrastructure code that:
- Will be reused across multiple projects
- Represents a clear, single-purpose component
- Has well-defined inputs and outputs
- Provides value as a standalone unit

For example, a module might handle:
- VPC creation with standard networking
- EKS node group configuration
- Standard S3 bucket setups
- RDS instance deployment

## Projects (The Houses)

A **project** is a complete infrastructure solution that combines modules to achieve a specific goal. Like a house blueprint, projects:

- Define the overall architecture
- Specify how modules work together
- Handle environment-specific configurations
- Manage dependencies between components

### The Environment Project

A special type of project is the "environment" project, which:
- Creates the foundational infrastructure
- Sets up shared resources
- Establishes networking boundaries
- Serves as a dependency for other projects

### When to Create a Project

Create a new project when you need to:
- Deploy a complete infrastructure solution
- Combine multiple modules for a specific purpose
- Manage environment-specific configurations
- Create isolated infrastructure components

For example, a project might be:
- "My AWS EKS Cluster" - combining networking, cluster, and node group modules
- "Data Platform" - combining storage, compute, and security modules
- "Web Application" - combining application, database, and caching modules

## Evolution and Maintenance

As your infrastructure grows:
- **Modules** should remain stable and focused
- **Projects** adapt to changing requirements
- New modules are added to the registry
- Existing projects are updated to use new module versions

Remember: Good organization of modules and projects leads to:
- Easier maintenance
- Better reusability
- Clearer documentation
- Simplified collaboration