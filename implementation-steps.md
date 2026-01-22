# 🛠 Implementation Steps – Tor Relay Node Setup (Middle Relay)

## Step 1: Install Tor on Ubuntu
Tor is installed using the official Ubuntu repositories.

```bash
sudo apt update
sudo apt install tor -y

### **Step 2: Verify Tor Installation**

tor --version

## Step 3: Check Tor Service Status
Ensure that the Tor service is running.

systemctl status tor

Expected result: Status should show active (running).

## Step 4: Configure Tor as a Middle Relay

Edit the Tor configuration file.

sudo nano /etc/tor/torrc

Add the following lines:
RunAsDaemon 1
ORPort 9001
Nickname MiddleRelayNode
ContactInfo admin@example.com
RelayBandwidthRate 100 KB
RelayBandwidthBurst 200 KB
ExitRelay 0
Save and exit the file.

## Step 5: Restart Tor Service

Apply the configuration changes.
sudo systemctl restart tor

## Step 6: Verify Tor is Running as a Process

Confirm that Tor is running in the background.
ps aux | grep tor

Expected result: Tor process should be listed.

## Step 7: Verify Logs 

Check Tor logs to ensure there are no errors.
journalctl -u tor --no-pager | tail

## Step 8: Confirmation of Middle Relay Setup

The system now acts as a Tor Middle Relay, safely routing encrypted traffic without exit functionality.
Verification is done using:
- Tor version output
- systemctl status
- torrc configuration
- running process list
- screenshots included in the project
