# Docker on AWS EC2

## 1. Install Docker

```bash
sudo yum install docker -y
```

---

## 2. Start Docker Service

```bash
sudo service docker start
```

Alternative:

```bash
sudo systemctl start docker
```

---

## 3. Check Docker Version

```bash
docker --version
```

Detailed:

```bash
sudo docker version
```

---

## 4. Login to DockerHub

```bash
sudo docker login
```

---

## 5. Check Docker Images

```bash
sudo docker images
```

---

## 6. Pull Ubuntu Image

```bash
sudo docker pull ubuntu
```

---

## 7. Create Dockerfile

```bash
nano Dockerfile
```

---

## 8. Dockerfile Contents

```dockerfile
FROM ubuntu:latest

LABEL maintainer="Ayush"

RUN apt-get update
```

---

## 9. Build Docker Image

```bash
sudo docker build -t image_name .
```

Example:

```bash
sudo docker build -t myubuntu .
```

---

## 10. Verify Created Image

```bash
sudo docker images
```

---

## 11. Run Container

```bash
sudo docker run -it ubuntu
```

Run in background:

```bash
sudo docker run -d ubuntu
```

---

## 12. View Running Containers

```bash
sudo docker ps
```

All containers:

```bash
sudo docker ps -a
```

---

## 13. Tag Docker Image

```bash
sudo docker tag local_image username/image_name:tag
```

Example:

```bash
sudo docker tag myubuntu ayush/myubuntu:1.0
```

---

## 14. Push Image to DockerHub

```bash
sudo docker push username/image_name:tag
```

Example:

```bash
sudo docker push ayush/myubuntu:1.0
```

---

# Docker Workflow

```text
Install Docker
      ↓
Start Docker
      ↓
Create Dockerfile
      ↓
Build Image
      ↓
Run Container
      ↓
Push to DockerHub
```