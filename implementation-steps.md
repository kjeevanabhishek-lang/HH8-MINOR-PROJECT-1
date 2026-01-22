```md
## Step 1: Install Tor on Ubuntu

Tor is installed using the official Ubuntu repositories.

```bash
sudo apt update
sudo apt install tor -y

```md
## Step 2: Verify Tor Installation

Verify that Tor is installed correctly.

```bash
tor --version

---

### 🔹 Step 3
```md
## Step 3: Check Tor Service Status

Ensure that the Tor service is running.

```bash
systemctl status tor
