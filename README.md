# qBittorrent-Enhanced-Edition-Docker

| Architecture | Tag            |
| :----------: | :------------: |
| x86-64       | latest   |
| arm64        | latest |
| arm32        | latest |

**qBittorrent Enhanced Edition**

```yaml
version: "2.0"
services:
  qbittorrentee:
    image: NightHammer1000/qbittorrentee:latest
    container_name: qbittorrentee
    restart: always
    tty: true
    network_mode: bridge
    hostname: qbittorrentee
    volumes:
      - ./data:/data      
    tmpfs:
      - /tmp
    environment:          
      - WEBUI_PORT=8080  
      - BT_PORT=34567    
      - PUID=1000         
      - PGID=100         
    ports:
      - 8080:8080     
      - 34567:34567 
      - 34567:34567/udp
```
