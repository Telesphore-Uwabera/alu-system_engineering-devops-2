
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
