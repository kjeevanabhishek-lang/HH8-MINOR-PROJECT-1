# STEP 1: Install Tor on Ubuntu
sudo apt update
`sudo apt install tor -y`

# STEP 2: Verify Tor Installation
tor --version

# STEP 3: Check Tor Service Status
systemctl status tor
#Expected: active (running)

# STEP 4: Configure Tor as a Middle Relay
sudo nano /etc/tor/torrc

#Add the following lines in torrc:
RunAsDaemon 1
ORPort 9001
Nickname MiddleRelayNode
ContactInfo admin@example.com
RelayBandwidthRate 100 KB
Relay Bandwidth Burst 200 KB
ExitRelay 0

#Save and exit (CTRL+O, Enter, CTRL+X)

# STEP 5: Restart Tor Service
 sudo systemctl restart tor 

# STEP 6: Verify Tor Service After Reboot systemctl status tor 
#Expected: active (running) 

# STEP 7: Verify Tor Process is Running 
ps aux | grep tor 

# STEP 8: Tor Logs Check 
journalctl -u tor --no-pager | tail
