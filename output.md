# Output 1: Tor Installed Successfully
#Command used to verify Tor installation and service
tor --version

#Expected: Tor version information displayed
systemctl status tor

#Expected: active (running)

# Output 2: Tor Configuration File Accessed
sudo nano /etc/tor

#Expected: torrc file opens with Middle Relay configuration

# Output 3: Tor process is running?
ps aux | grep tor # Expected: tor daemon process visible 

# Output 4: Tor Logs Verification 
journalctl -u tor --no-pager | tail 

#Expected: No critical errors, service running normally
