The below guide focuses on setting up a Plex server with a Synology NAS

On the Synology NAS create the media folder.

<img width="1342" height="838" alt="image" src="https://github.com/user-attachments/assets/d8dbbbdf-4b70-4751-8978-45f3a5931a5e" />

Create the TV and Movie folders

<img width="1050" height="615" alt="image" src="https://github.com/user-attachments/assets/335bf837-9e94-4275-a9e4-0a30de4d8d9a" />

Create a new user under the Synology NAS

<img width="1177" height="741" alt="image" src="https://github.com/user-attachments/assets/be06d216-6050-4450-bede-e0a9e6f14612" />

Give the user access to the media folder

<img width="884" height="673" alt="image" src="https://github.com/user-attachments/assets/fe2170d6-d6d1-4821-86cd-c53798720a17" />

**Install SMP support on Ubuntu**

``` sudo apt update ```

sudo apt install cifs-utils

**Create an empty directory**

sudo mkdir -p /mnt/media

**Mount the NAS inside the media directory (Show the contents of //192.168.1.20/Media inside /mnt/media)**

sudo mount -t cifs //192.168.1.20/Media /mnt/media -o username=plex,password=YourPassword

**To verify:**

cd /mnt/media
lt -1

<img width="328" height="152" alt="image" src="https://github.com/user-attachments/assets/282d09d4-68c0-432f-bbc6-f473d8f48ffc" />

**To verify the network drive**

df -h

<img width="727" height="188" alt="image" src="https://github.com/user-attachments/assets/0251dfc6-97d2-4bf7-9cba-bfa8b57e6320" />

**Create a directory for Plex Database Metadata**

sudo mkdir -p /opt/plex/config

**Create Plex project folder (can be under your home diretory)**

``` mkdir ~/plex ```

``` cd ~/plex ```

**Create the Docker Compose File**

```
nano docker-compose.yml
```

**Paste this:**

```yaml
services:
  plex:
    image: lscr.io/linuxserver/plex:latest
    container_name: plex
    network_mode: host
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Australia/Sydney
      - VERSION=docker
    volumes:
      - /opt/plex/config:/config
      - /mnt/media/Movies:/movies
      - /mnt/media/TV:/tv
    restart: unless-stopped
```

 **Enter ctrl + O and ctrl + X to save**

  **To Start Plex run:**

```
  sudo docker compose up -d
```

<img width="1245" height="136" alt="image" src="https://github.com/user-attachments/assets/eb47885d-c5f7-49e4-b618-9a9556ed8906" />

To verify:

```
docker ps
```
**Now head over to your IP and confirm Plex is installed**

http://192.168.20.20:32400/web

Sign up with Plex with a Free account and add the media libraries we created before

<img width="786" height="789" alt="image" src="https://github.com/user-attachments/assets/f96aa754-5409-47af-bb51-b13eac606b89" />





    

    
