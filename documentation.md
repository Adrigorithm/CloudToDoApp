# Documentation

## Initial Setup
- Create 3 `Amazon Linux 2023` EC2 instances
- Expose port `22` on all instances for IPs from which you wish to shell in to.
- Run `setup` playbook
- Run `copyDirectories` playbook

### Frontend
- docker build -t frontend --build-arg APIURL=http://172.31.25.118:8090 ./frontend

**`APIURL`** should match the ip and port exposed on the machine running the `backend`.

- sudo docker run -d --name frontend -p 80:80 frontend
- confirm the site is live by accessing its public ip address.
![frontend](images/frontend.png)

### Backend

### Database