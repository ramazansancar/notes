# Raspberry Pi Legacy Setup Commands

## Update && Upgrade && Dist-Upgrade && Autoremove Commands

```bash
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get dist-upgrade -y
sudo apt-get autoremove -y
```

## System Monitoring Tools Installation

```bash
sudo apt install bpytop -y
```


## NVM Inslallation (Node Version Manager)

```bash
#https://github.com/nvm-sh/nvm?tab=readme-ov-file#install--update-script
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash

```

## Node.js Installation

```bash
nvm install 20
nvm use 20
```

## PM2 && PNPM (Optional) Installation

```bash
npm -g install pm2 pnpm
```

### PM2 Commands

```bash
# https://pm2.keymetrics.io/docs/usage/startup/#generate-startup-script
pm2 startup
# Copy the command and run it

# https://pm2.keymetrics.io/docs/usage/startup/#saving-the-app-list-to-be-restored-at-reboot
pm2 save

# https://pm2.keymetrics.io/docs/usage/startup/#manually-resurrect-processes
pm2 resurrect

# List PM2 Processes (Apps)
pm2 ls
```

## Git && Python3 && Python3-pip Installation

```bash
sudo apt install git python3 python3-pip -y
```

## Docker Installation

```bash
#https://docs.docker.com/engine/install/debian/
curl -fsSL -o- https://get.docker.com | bash

# Check Docker Version (Installed or Not)
docker --version
```

## Docker Compose Installation

```bash
#https://docs.docker.com/compose/install/
sudo apt install docker-compose -y
```

## Docker Watchtower Installation (Auto Update Docker Containers)

```bash
#
sudo docker run -d --restart=always --name watchtower -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower
```

## Pi-hole Installation

```bash
# Important: Change {username} with your username
sudo mkdir /home/{username}/pihole
cd /home/{username}/pihole
curl -o docker-compose.yml https://raw.githubusercontent.com/pi-hole/docker-pi-hole/master/examples/docker-compose.yml.example > docker-compose.yml
sudo docker-compose up -d
```

### Pi-hole Update Script (Optional)

```bash
cd /home/{username}/pihole

## Create update.sh file
touch update.sh && chmod +x update.sh #Optional
echo "sudo docker-compose down" > update.sh
echo "sudo docker-compose pull" >> update.sh
echo "sudo docker-compose up -d" >> update.sh
```

### Uptime Kuma Installation

```bash
sudo docker run -d --restart=always -p 9999:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
```

### FreshRSS Installation

```bash
# Important: Change {username} with your username
sudo docker run -d --restart unless-stopped --log-opt max-size=10m -p 8888:80 -e TZ=Europe/Istanbul -e 'CRON_MIN=1,31' -v /home/{username}/freshrss/data:/var/www/FreshRSS/data -v /home/{username}/freshrss/extensions:/var/www/FreshRSS/extensions --name freshrss freshrss/freshrss
```

## Docker Image Cleanup (Remove Unused Docker Images)

```bash
# 
sudo docker image prune

# Old Commands
#https://gist.github.com/bastman/5b57ddb3c11942094f8d0a97d461b430
```

## Docker Container Cleanup (Remove Exited Docker Containers)

```bash
#https://gist.github.com/bastman/5b57ddb3c11942094f8d0a97d461b430
docker rm $(docker ps -a | grep "Exited" | awk "{print $1}")
```

## Static IP Configuration

```bash
#https://www.raspberrypi.org/documentation/configuration/tcpip/
sudo nano /etc/dhcpcd.conf

# Add the following lines to the end of the file
interface eth0
static ip_address=192.168.1.200
static routers=192.168.1.1
static domain_name_servers=1.0.0.1

# Save the file and exit
sudo reboot

# Check the IP Address
ip a

```
