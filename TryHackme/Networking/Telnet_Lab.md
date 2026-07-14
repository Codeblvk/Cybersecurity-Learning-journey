# Telnet Lab

## Objective

Learn how telnet can connect to different TCP ports

## Port 7 -Echo Service 

Command:
'telnet 10.49.153.238 7'

### Observation

- Text entered is echoed back.
- Demonstrates an Echo service

## Port 13 -Daytime Service

command:
'telnet 10.49.153.238 13'

### Observation

- Server returned the current date and time.
- Connection closed automatically

### Screenshot

![Port 7 Echo service and port 13 day time service](/TryHackme/Screenshot/port7%20and%2013.png)

### Note 

Echo and day time services are considered security risk and should not be run. As they lack encryption and exposes system unnecessarly.

## Port 80 -HTTP Request 

### Command

'telnet 10.49.153.238 80'

### HTTP Request

```http
GET / HTTP/1.1
Host: telnet.thm
```

### Observation

- Server returned HTTP 200 OK.
- Received a web page response.

### Screenshot
![Port 80 HTTP Request](/TryHackme/Screenshot/port80.png)