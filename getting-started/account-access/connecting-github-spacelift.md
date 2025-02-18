---
layout: default
title: Connecting GitHub to Spacelift
nav_order: 3
parent: Account Access
grand_parent: Getting Started
permalink: /getting-started/account-access/connecting-github-spacelift/
---
# getting-started/account-access/connecting-github-spacelift.md
## Connecting GitHub and Spacelift

To streamline the workflow and enable seamless integration between GitHub and Spacelift, you'll need to connect your GitHub account and repositories to Spacelift. This allows Spacelift to access your Terraform code stored in GitHub and manage the infrastructure deployment process.

### Connecting GitHub to Spacelift

1. Log in to your Spacelift account and navigate to your organization.
2. Click on the "Integrations" tab and select "GitHub" from the list of available integrations.
3. Follow the prompts to authorize Spacelift to access your GitHub account and repositories.
4. Once the integration is set up, you can select the GitHub repositories you want to connect to Spacelift.

### Creating a Spacelift Project

1. In Spacelift, navigate to your organization and click on the "Create Project" button.
2. Select the "GitHub" option as the source for your project.
3. Choose the GitHub repository containing your Terraform code.
4. Configure any additional settings or options as needed, such as specifying the Terraform working directory or variables.
5. Click "Create Project" to finalize the setup.

### Managing Workspaces and Runs

After creating your Spacelift project, you can manage workspaces and runs directly from the Spacelift interface:

1. Navigate to your project and click on the "Workspaces" tab.
2. Create a new workspace or select an existing one to manage.
3. Within a workspace, you can trigger Terraform runs (plan, apply, destroy) and view the output and logs.
4. Collaborate with your team by leaving comments, reviewing changes, and approving runs.

By connecting GitHub and Spacelift, you can streamline your infrastructure as code workflow, leverage version control for your Terraform code, and take advantage of Spacelift's powerful collaboration and deployment features.