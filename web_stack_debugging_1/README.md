
# Nginx Port Troubleshooting Script

This Bash script is designed to troubleshoot issues related to Nginx not listening on port 80 in an Ubuntu container. It performs the following tasks:

1. Replaces port 8080 with port 80 in the Nginx configuration.
2. Restarts the Nginx service.
3. Symlinks the default site configuration from `sites-available` to `sites-enabled`.
4. Restarts the Nginx service again.
5. Kills the first instance of the Nginx process to ensure a clean restart.

## Prerequisites

Before using this script, make sure you have:

- An Ubuntu container with Nginx installed.
- Appropriate permissions to modify Nginx configuration and restart the service.

## Usage

1. Copy the script to your Ubuntu container.
2. Make it executable using the following command:

   ```bash
   chmod +x your_script_name.sh
   ```

3. Execute the script as a superuser or with sudo privileges:

   ```bash
   sudo ./your_script_name.sh
   ```

## Notes

- This script assumes that the default Nginx configuration file is located at `/etc/nginx/sites-available/default`. Modify the script if your configuration file is located elsewhere.
- Always be cautious when modifying system configurations and restarting services.

## Author

Telesphore Uwabera

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

