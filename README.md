# Azure DevOps Branch Policies Template

This repository contains a reusable Azure DevOps Pipeline template that automatically checks and sets branch policies and permissions on a specified repository.

## Features

- Determines the default branch of the specified repository
- Checks and sets the following permissions on the default branch:
  - "Force Push" denied for everyone
  - "Edit Policies" denied for everyone
  - "Bypass policies when completing pull requests" denied for everyone
  - "Bypass policies when pushing" denied for everyone
- Checks and sets the following policies on the default branch:
  - Minimum number of contributors set to 2
  - Reset all approval votes when new changes are pushed
- Supports multiple deployment strategies:
  - Canary deployment: gradually roll out changes to a small subset of users before full deployment
  - Blue-Green deployment: reduces downtime by running two identical production environments

## Usage

### Basic Usage in Your Pipeline
