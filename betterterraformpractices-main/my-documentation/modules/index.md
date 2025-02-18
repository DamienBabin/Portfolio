---
layout: default
title: Modules
nav_order: 1
parent: Documentation
has_children: true
permalink: /modules/
---

# Infrastructure Modules

Our infrastructure modules are the building blocks of our cloud infrastructure. Each module is designed to be:
- Reusable across multiple projects
- Well-documented and maintained
- Configurable through variables
- Tested and verified

## Available Modules

### AWS Modules
- [AWS RDS Database](/modules/aws/rds-database/) - Managed relational database service
- [AWS EKS Cluster](/modules/aws/eks-cluster/) - Managed Kubernetes service
- [AWS ElastiCache Redis](/modules/aws/elasticache-redis/) - In-memory caching service

### Azure Modules
- [Azure Database](/modules/azure/database/) - Managed database services
- [Azure Kubernetes Cluster](/modules/azure/kubernetes-cluster/) - Azure Kubernetes Service (AKS)
- [Azure Redis Cache](/modules/azure/redis-cache/) - Managed Redis cache

## Module Structure

Each module follows our standard documentation structure:
1. Overview and purpose
2. Usage examples
3. Input variables
4. Output values
5. Resource specifications
6. Architecture diagrams

## Contributing

To contribute a new module:
1. Follow our [naming standards](/getting-started/important-concepts/4naming-standards/)
2. Use our [README template](/getting-started/important-concepts/3readme-guide/)
3. Include complete documentation
4. Submit through our standard PR process