
# Firewall Configuration and SSH Login Script

This repository contains a Bash script for configuring a UFW firewall to block all incoming traffic except for TCP ports 22, 80, and 443. It also includes SSH login scripts for connecting to remote servers.

## Firewall Configuration

The firewall configuration script (`firewall-config.sh`) sets up the following rules:

- Default incoming policy: Deny
- Default outgoing policy: Allow
- Allow incoming traffic on TCP ports 22, 80, and 443
- Allow DHCP client traffic
- Allow ICMP packets for various types
- Allow multicast mDNS and UPnP for service discovery

### Usage

To configure the firewall, follow these steps:

1. Install UFW (Uncomplicated Firewall):

   ```bash
   sudo apt install ufw
   ```

2. Run the firewall configuration script:

   ```bash
   sudo bash firewall-config.sh
   ```

## SSH Login Scripts

This repository also includes SSH login scripts (`server-01-login.sh`) for connecting to remote servers. These scripts simplify the login process by managing SSH agents and keys.

### Usage

To use the SSH login scripts, follow these steps:

1. Ensure you have an SSH key pair set up and that the private key is located in `~/.ssh/school`.

2. Run the desired SSH login script for the server you want to connect to. For example:

   ```bash
   bash server-01-login.sh
   ```

   Replace `server-01-login.sh` with the appropriate script for your target server.

## Author

Telesphore Uwabera

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
```

# Bash Script Automation

This repository contains a set of Bash scripts for automating the installation and configuration of Nginx, HAProxy, and SSH login to two servers.

## Prerequisites

Before running these scripts, make sure you have:

- A Linux-based system (Ubuntu in this case) where you intend to install Nginx and HAProxy.
- SSH access to the target servers with the necessary private key (`~/.ssh/school` in this case).
- Basic knowledge of Bash scripting and server administration.

## Usage

### Install and Configure Nginx

1. Run the `nginx-install.sh` script to install Nginx and configure it with a default server block.

   ```bash
   ./nginx-install.sh
   ```

2. The script will update packages, install Nginx, and create a default server block in `/etc/nginx/sites-available/default`.

### Install and Configure HAProxy

1. Run the `haproxy-install.sh` script to install and configure HAProxy.

   ```bash
   ./haproxy-install.sh
   ```

2. The script will update packages, install HAProxy, and configure it with backend server details.

### SSH Login to Servers

Use the following scripts to SSH into the respective servers:

- For Server 1:

   ```bash
   ./server-01-login.sh
   ```

- For Server 2:

   ```bash
   ./server-02-login.sh
   ```

These scripts will set up SSH agent forwarding and log you into the respective servers using the `~/.ssh/school` private key.

## Important Notes

- Make sure to update the IP addresses and server names in the HAProxy configuration to match your specific setup.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```


**First Script:**

```bash
#!/usr/bin/env bash
# Connects to server 35.172.230.83 with key in ~/.ssh/school

ssh -i ~/.ssh/school ubuntu@41.173.28.234
```

This script is meant to connect to a remote server at IP address `41.173.28.234` using SSH. It specifies the identity file (private key) located at `~/.ssh/school` for authentication and connects as the `ubuntu` user.

**Second Script:**

```bash
#!/usr/bin/env bash
# Creates RSA key pair

ssh-keygen -t rsa -b 4096 -f school -N "betty"
```

This script generates an RSA key pair using `ssh-keygen`. It creates a private key file named `school` and a corresponding public key file named `school.pub`. The `-N "betty"` option sets a passphrase for the private key (you should replace "betty" with your desired passphrase).

**Configuration Settings:**

The provided configuration settings seem to be related to SSH configuration and setup. Here's what they do:

1. `file_line` resource for turning off password authentication:
   - This block modifies the `/etc/ssh/ssh_config` file to disable password authentication by adding the line `PasswordAuthentication no`.

2. `file_line` resource for declaring the identity file:
   - This block modifies the `/etc/ssh/ssh_config` file to specify the identity file as `~/.ssh/school`.

3. SSH configuration settings:
   - Below the configuration resources, there seems to be an attempt to configure SSH settings for all hosts using a wildcard `Host *`. However, there is a typo: it should be `IdentityFile` instead of `IdentifyFile`. It should also be placed in the `~/.ssh/config` file (not `/etc/ssh/ssh_config`) if you want these settings to apply only to your user.
