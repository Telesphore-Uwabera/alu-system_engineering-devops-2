
# Bash Scripts and HTML Documentation

This repository contains a collection of Bash scripts and an HTML file. These scripts perform various tasks related to server configuration and file transfer.

## Table of Contents

- [File Transfer Script](#file-transfer-script)
- [Nginx Installation and Configuration Script](#nginx-installation-and-configuration-script)
- [Redirecting Script](#redirecting-script)
- [404 Page Configuration Script](#404-page-configuration-script)
- [Custom 404 HTML Page](#custom-404-html-page)
- [Server Login Script](#server-login-script)

## File Transfer Script

`transfer_file.sh` is a Bash script used to transfer a file from a client to a server using SCP.

Usage:
```bash
./transfer_file.sh PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY
```

## Nginx Installation and Configuration Script

`install_nginx.sh` is a Bash script that installs Nginx and configures it to listen on port 80.

## Redirecting Script

`redirect.sh` is a Bash script that configures an Nginx server to redirect requests to another page.

## 404 Page Configuration Script

`404_page.sh` is a Bash script that configures an Nginx server to respond with a custom 404 error page.

## Custom 404 HTML Page

The `404.html` file is a custom HTML page designed to be displayed when a 404 error occurs on the Nginx server.

## Server Login Script

`server_login.sh` is a Bash script that sets up SSH agent and logs in to a server.

---

