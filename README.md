# Proxy Formatter

This script is used to format a list of proxies into a standard format. The proxy format that the script produces is:  
`http://user:pass@ip:port`.

## Supported Formats

The script supports the following proxy formats:
- `ip:port:user:pass` → Formatted into `http://user:pass@ip:port`
- `ip:port` → Assumes default values for `user` and `pass`
- `ip:port:user` → Assumes default `pass`

## Prerequisites

Ensure you have Node.js installed on your machine. If not, you can download it from [Node.js official website](https://nodejs.org/).

## Usage

### 1. Clone the Repository

```bash
git clone <repository_url>
cd <repository_folder>
```

### 2. Prepare the Input File

Create a file named `inproxy.txt` in the same directory as the script. This file should contain a list of proxies in one of the supported formats, one proxy per line.

Example inproxy.txt:

```bash
192.168.1.1:8080:user:password
10.0.0.1:9090
172.16.0.1:8000:proxyuser
```

### 3. Run the Script

Open your terminal or command prompt, navigate to the folder containing the script, and run the following command:

```bash
node convert.js
```
### 4. Check the Output

The script will generate an output file named `outproxy.txt` in the same directory. The file will contain the formatted proxies.

Example outproxy.txt:

```bash
http://user:password@192.168.1.1:8080
http://user:pass@10.0.0.1:9090
http://proxyuser:pass@172.16.0.1:8000
```
