# hello-smtp

Detailed acquaintance with the SMTP protocol.

### How to use?

1. Run local SMTP server.

```bash
docker-compose up
```

2. Establish connection

```bash
telnet 127.0.0.1 10025
```

Now wait for first message with server version and current date.

After that send commands:

```text
EHLO
EHLO smtp.example.com
MAIL FROM:sergey@gmail.com
RCPT TO:valera@smtp.example.com
DATA
```
Mail body ends with "." placed on separate line.

```text
Hello, Valera! Hope you doing well!
.
```

Last command close connection:

```text
QUIT
```