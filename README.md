# Vagrant + Ansible Node.js Deployment

This project automates the deployment of a Node.js application using Vagrant for VM management and Ansible for configuration management.

## Overview

- **Vagrant**: Creates and manages an Ubuntu 22.04 (Jammy) virtual machine
- **Ansible**: Provisions the VM and deploys a Node.js application
- **Target App**: Deploys a Node.js app from GitHub repository

## Prerequisites

- Vagrant installed
- VirtualBox installed
- Ansible installed on host machine

## Configuration

### VM Specifications
- **OS**: Ubuntu 22.04 LTS (Jammy)
- **Memory**: 2048 MB
- **CPUs**: 2
- **Network**: Private network (192.168.56.101)

### Application Details
- **Node.js Version**: 16.x
- **Source**: https://github.com/priyabuss2004/node-app.git
- **Deployment Path**: `/home/vagrant/node-app`

## Usage

1. **Start the VM**:
   ```bash
   vagrant up
   ```

2. **Run Ansible Playbook**:
   ```bash
   ansible-playbook -i inventory main.yml
   ```

3. **Access the Application**:
   - VM IP: 192.168.56.101
   - Check application logs in `/home/vagrant/node-app/app.log`

## Files

- `Vagrantfile` - VM configuration
- `main.yml` - Ansible playbook for Node.js deployment
- `inventory` - Ansible inventory file with VM connection details

## Commands

```bash
# Start VM
vagrant up

# SSH into VM
vagrant ssh

# Stop VM
vagrant halt

# Destroy VM
vagrant destroy
```
