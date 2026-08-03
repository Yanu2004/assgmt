## Output of `sudo ss -tulpn | grep :80`
```sudo ss -tulpn | grep :80
tcp   LISTEN 0      511          0.0.0.0:80        0.0.0.0:*    users:(("nginx",pid=120089,fd=5),("nginx",pid=120088,fd=5),("nginx",pid=120087,fd=5),("nginx",pid=120086,fd=5),("nginx",pid=120085,fd=5))
tcp   LISTEN 0      511             [::]:80           [::]:*    users:(("nginx",pid=120089,fd=6),("nginx",pid=120088,fd=6),("nginx",pid=120087,fd=6),("nginx",pid=120086,fd=6),("nginx",pid=120085,fd=6))
```
## Output of `sudo journalctl -u nginx -n 20`
```sudo journalctl -u nginx -n 20
Aug 01 11:42:38 vmi3471188 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Aug 01 11:42:38 vmi3471188 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
Aug 03 15:41:32 vmi3471188 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server...
Aug 03 15:41:32 vmi3471188 systemd[1]: nginx.service: Deactivated successfully.
Aug 03 15:41:32 vmi3471188 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
Aug 03 15:42:58 vmi3471188 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Aug 03 15:42:58 vmi3471188 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
Aug 03 15:43:32 vmi3471188 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server...
Aug 03 15:43:32 vmi3471188 systemd[1]: nginx.service: Deactivated successfully.
Aug 03 15:43:32 vmi3471188 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
Aug 03 15:43:32 vmi3471188 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Aug 03 15:43:32 vmi3471188 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
```
## Difference between `kill -15` and `kill -9`
`Kill -15` (SIGTERM) asks a process to terminate gracefully. It allows the process to clean up and exit normally.
`Kill -9` (SIGKILL) immediately forces the process to stop without allowing it to clean up or save its state.
