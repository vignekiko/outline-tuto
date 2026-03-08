# Outline
# Install Docker
    sudo apt update && sudo apt install docker.io -y
# Run this command 
    sudo bash -c "$(wget -qO- https://raw.githubusercontent.com/Jigsaw-Code/outline-server/master/src/server_manager/install_scripts/install_server.sh) --hostname <put your Reserved-IP>"
    
# 🛡️ Outline Server Maintenance Notes

### 1. Status Check
To see if your server is running, use:
    ```bash
         docker ps
        docker logs shadowbox
            ```
### 2. Network Debug
- If you have connection issues, run these:
   ```bash
        ping github.com
        netstat -tulpn | grep LISTEN
        sudo ufw status
   ```
- Verify if the server has an active outbound internet connection :
  ```bash
    ping github.com
    ```
- Check if the required ports are actually open and listening for traffic :
  ```bash
    netstat -tulpn | grep LISTEN
    ```
- Check if the server's internal firewall (Uncomplicated Firewall) is blocking incoming connections :
  ```bash
    sudo ufw status
    ```
### Troubleshooting
- Install Docker
  ```bash
  sudo apt install docker.io -y
  ```
- Check IP
  ```bash
  curl ifconfig.me
  ```

  

