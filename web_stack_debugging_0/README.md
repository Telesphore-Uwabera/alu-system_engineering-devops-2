
# Container Web Server Setup

This set of Bash scripts is designed to help you set up web servers on designated containers. It includes scripts for configuring both Apache and Nginx servers to listen on port 80.

## Apache Configuration

The `apache_setup.sh` script performs the following tasks for Apache:

1. Appends `ServerName localhost` to the `/etc/apache2.conf` configuration file.
2. Starts the Apache service.

To use this script:

```bash
./apache_setup.sh
```

## Nginx Configuration

The `nginx_setup.sh` script fixes Nginx's listening on port 80. It does the following:

1. Navigates to the `/etc/nginx/sites-enabled/` directory.
2. Deletes the default configuration file (if it exists).
3. Creates a symbolic link to the default configuration file from `/etc/nginx/sites-available/`.
4. Restarts the Nginx service.

To use this script:

```bash
./nginx_setup.sh
```
