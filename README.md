# OVERVIEW

# This project sets up multiple Vagrant virtual machine environments with distinct configurations to support various development and deployment scenarios. Each Vagrantfile is tailored to provision specific environments such as web servers, database servers, and a WordPress hosting setup.

# 1 WordPress Hosting Environment

# Description:This Configures a Vagrant machine for hosting a WordPress site.

# Base Box: ubuntu/focal64

# Features : includes the following

# Sets up a private network (192.168.56.30) and a public network.

# Provisions WordPress and Apache with required PHP and MySQL dependencies.

# Automates database creation with user credentials and configures WordPress.

# Usage:Brings up the machine: vagrant up

# Access the WordPress site on the configured IP address.

# 2 Multi-Machine Web & Database Environment

# Description: Defines three VMs (web01, web02, db01) for web server and database operations.

# Machine Details: this involves 2 web servers

# web01 and web02:

# Base Box: ubuntu/focal64

# Roles: Web servers

# Network: Private (IPs 192.168.56.41, 192.168.56.43)

# db01:

# Base Box: centos/7

# Role: Database server

# Network: Private (IP 192.168.56.42)

# Provisions and starts MariaDB with default configurations.

# Usage:Start all machines: vagrant up

# Access web servers via their respective private IPs.

# Database available on db01 machine.

# 3 CentOS-Based Finance Site Deployment

# Description: Configures a Vagrant machine for a finance site using CentOS 7 as the base

# Base Box: eurolinux-vagrant/centos-stream-9

# Features:

# Configures private and public networks.

# Provisions Apache, downloads, and installs a finance template from tooplate.com.

# Enables services and sets up a web directory.

# Usage:

# Bring up the machine: vagrant up

# Access the site on the configured IP or via the host network.

# Prerequisites

# Vagrant: Install Vagrant (https://www.vagrantup.com/).

# VirtualBox: Ensure VirtualBox is installed as the provider.
