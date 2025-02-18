---
layout: default
title: Naming Standards
nav_order: 4
parent: Important Concepts
grand_parent: Getting Started
permalink: /getting-started/important-concepts/4naming-standards/
---

# Naming Standards

Clear and consistent naming conventions are crucial for maintaining a scalable and manageable infrastructure codebase. These standards help ensure clarity, prevent conflicts, and make resources easily identifiable.

## Repository Naming

### Module Repositories
- Format: `terraform-{cloud}-{resource}`
- Purpose: Reusable infrastructure components
- Examples:
  - `terraform-aws-eks-node-group`
  - `terraform-aws-rds-instance`
  - `terraform-gcp-kubernetes-cluster`

### Project Repositories
- Format: `tfp-{org}-{purpose}`
- Purpose: Complete infrastructure solutions
- Examples:
  - `tfp-acme-data-platform`
  - `tfp-acme-eks-prod`
  - `tfp-acme-shared-services`

### Workspace Management Repositories
- Format: `tfw-{org}-{business-unit}`
- Purpose: Spacelift stack and variable management
- Examples:
  - `tfw-acme-platform-team`
  - `tfw-acme-data-team`
  - `tfw-acme-shared-services`

## Branch Naming

### Standard Branches
- `main` - Production-ready code
- `qa` - Quality assurance testing
- `dev` - Development and integration

### Feature Branches
- Format: `feature/{ticket-number}-{brief-description}`
- Example: `feature/INFRA-123-add-backup-retention`

### Bugfix Branches
- Format: `bugfix/{ticket-number}-{brief-description}`
- Example: `bugfix/INFRA-456-fix-subnet-routing`

## Resource Naming

### General Pattern
- Format: `{org}-{env}-{purpose}-{resource}`
- Examples:
  - `acme-prod-app-eks`
  - `acme-dev-shared-vpc`
  - `acme-qa-data-rds`

### Environment Abbreviations
- `prod` - Production
- `qa` - Quality Assurance
- `dev` - Development

## Variable Naming

### Terraform Variables
- Use descriptive, lowercase names with underscores
- Format: `{resource}_{purpose}_{attribute}`
- Examples:
  - `vpc_cidr_range`
  - `eks_node_instance_type`
  - `rds_backup_retention_days`

### Spacelift Variables
- Environment-specific: `{ENV}_{VARIABLE_NAME}`
- Global: `GLOBAL_{VARIABLE_NAME}`
- Examples:
  - `PROD_AWS_ACCOUNT_ID`
  - `DEV_VPC_CIDR`
  - `GLOBAL_REGION`

## Best Practices

1. **Consistency**
   - Follow established patterns
   - Use lowercase for repository names
   - Use underscores for variable names

2. **Clarity**
   - Names should be self-descriptive
   - Avoid abbreviations except for established standards
   - Include purpose in resource names

3. **Organization**
   - Include organization identifier where appropriate
   - Use environment indicators for environment-specific resources
   - Follow business unit boundaries

4. **Maintainability**
   - Keep names concise but meaningful
   - Document any deviations from standards
   - Review naming conventions periodically