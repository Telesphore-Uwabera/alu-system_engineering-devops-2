
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
