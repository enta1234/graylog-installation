# Graylog Installation
##  1. Installation

### Prerequisites

Ensure you have the following prerequisites installed and configured on your system:

- Docker: Download and install Docker from [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)

**How to generate new password for default.**

GRAYLOG_PASSWORD_SECRET

```bash
pwgen -N 1 -s 96
```

GRAYLOG_ROOT_PASSWORD_SHA2

```bash
echo -n "yourpassword" | shasum -a 256
```

Replace them in ```docker-compose.yml```

### Starting Graylog Compose

```bash
docker-compose up -d
```

## 4. Usage

### Accessing Graylog Web Interface

1. Open a web browser and navigate to the following URL:

```
http://localhost:9000
```

2. Login using the default credentials:

```
Username: admin
Password: yourpassword
```