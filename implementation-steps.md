## Step 1: Install Tor on Ubuntu

Tor is installed using the official Ubuntu repositories.

```bash
sudo apt update
sudo apt install tor -y

tor --version

systemctl status tor
