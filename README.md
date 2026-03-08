# Outline
# Install Docker
    sudo apt update && sudo apt install docker.io -y
# Run this command 
    sudo bash -c "$(wget -qO- https://raw.githubusercontent.com/Jigsaw-Code/outline-server/master/src/server_manager/install_scripts/install_server.sh) --hostname <put your Reserved-IP>"
## Outline Server Status Check
 Use this to check if Outline containers (specifically the shadowbox container) are active and running
    ```sh
    docker ps
    ```
### Use this to view detailed error logs and debug internal service issues
    docker logs shadowbox
## Network and Port Debugging
### Verify if the server has an active outbound internet connection
    ping github.com
### Check if the required ports are actually open and listening for traffic
    netstat -tulpn | grep LISTEN
### Check if the server's internal firewall (Uncomplicated Firewall) is blocking incoming connections
    sudo ufw status
## Troubleshooting
### Docker Not Found (Docker ကိုမတွေ့ရင်)
    sudo apt install docker.io -y
   - API URL not connecting ဖြစ်နေရင်  (Reserved IP နဲ့ Firewall Port ဖွင့်တာ ပြန်စစ်ပေးပါရန်)
