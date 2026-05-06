# Creating an EC2 Instance

## 1. Open EC2 Service

```text
Services → EC2
```

---

## 2. Launch Instance

Click:

```text
Launch Instances
```

---

## 3. Configure Instance

- Enter instance name
- Select Amazon Linux
- Select Free Tier Eligible AMI
- Choose t2.micro or t3.micro

---

## 4. Configure Key Pair

You can:
- Create key pair
OR
- Proceed without key pair

---

## 5. Configure Network Settings

Enable:
- HTTP traffic
- HTTPS traffic

Optional:
- SSH traffic

---

## 6. Launch Instance

Click:

```text
Launch Instance
```

---

## 7. Connect to EC2

Select instance.

Click:

```text
Connect
```

Then:

```text
EC2 Instance Connect → Connect
```

---

## 8. Install Docker

```bash
sudo yum install docker -y
```

Start Docker:

```bash
sudo service docker start
```

---

## 9. Stop or Terminate Instance

After work completion:

```text
Instance State → Stop Instance
```

OR

```text
Instance State → Terminate Instance
```

---

# EC2 Workflow

```text
Launch EC2
     ↓
Connect to EC2
     ↓
Install Docker
     ↓
Create Docker Images
     ↓
Push Images to DockerHub
     ↓
Stop or Terminate EC2
```