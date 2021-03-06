<h1 align="center">
  <img src="static/simplehttpserver-logo.png" alt="simplehttpserver" width="200px"></a>
  <br>
</h1>

[![License](https://img.shields.io/badge/license-MIT-_red.svg)](https://opensource.org/licenses/MIT)
[![Go Report Card](https://goreportcard.com/badge/github.com/projectdiscovery/simplehttpserver)](https://goreportcard.com/report/github.com/projectdiscovery/simplehttpserver)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/projectdiscovery/simplehttpserver/issues)
[![GitHub Release](https://img.shields.io/github/release/projectdiscovery/simplehttpserver)](https://github.com/projectdiscovery/simplehttpserver/releases)
[![Follow on Twitter](https://img.shields.io/twitter/follow/pdiscoveryio.svg?logo=twitter)](https://twitter.com/pdiscoveryio)
[![Docker Images](https://img.shields.io/docker/pulls/projectdiscovery/simplehttpserver.svg)](https://hub.docker.com/r/projectdiscovery/simplehttpserver)
[![Chat on Discord](https://img.shields.io/discord/695645237418131507.svg?logo=discord)](https://discord.gg/KECAGdH)

simplehttpserver is a go enhanced version of the well known python simplehttpserver.

# Resources

- [Features](#features)
- [Usage](#usage)
- [Installation Instructions](#installation-instructions)
- [Running simplehttpserver](#running-simplehttpserver-in-the-current-folder )
- [Thanks](#thanks)

# Features

<h1 align="left">
  <img src="static/simplehttpserver-run.png" alt="simplehttpserver" width="700px"></a>
  <br>
</h1>

 - File server in arbitrary directory
 - Full request/response dump
 - Configurable ip address and listening port


# Installation Instructions


### From Binary

The installation is easy. You can download the pre-built binaries for your platform from the [Releases](https://github.com/projectdiscovery/simplehttpserver/releases/) page. Extract them using tar, move it to your `$PATH`and you're ready to go.

```sh
Download latest binary from https://github.com/projectdiscovery/simplehttpserver/releases

▶ tar -xvf simplehttpserver-linux-amd64.tar
▶ mv simplehttpserver-linux-amd64 /usr/local/bin/simplehttpserver
▶ simplehttpserver -h
```

### From Source

simplehttpserver requires **go1.14+** to install successfully. Run the following command to get the repo - 

```sh
▶ GO111MODULE=on go get -v github.com/projectdiscovery/simplehttpserver
```

### From Github

```sh
▶ git clone https://github.com/projectdiscovery/simplehttpserver.git; cd simplehttpserver; go build; mv simplehttpserver /usr/local/bin/; simplehttpserver -h
```

# Usage

```sh
simplehttpserver -h
```

This will display help for the tool. Here are all the switches it supports.

| Flag   | Description                                          | Example                                 |
| ------ | ---------------------------------------------------- | --------------------------------------- |
| listen | Configure listening ip:port (default 127.0.0.1:8000) | simplehttpserver -listen 127.0.0.1:8000 |
| path   | Fileserver folder (default current directory)        | simplehttpserver -path /var/docs        |
| v      | Verbose (dump request/response, default false)       | simplehttpserver -v                     |

### Running simplehttpserver in the current folder  

This will run the tool exposing the current directory on port 8000 

```sh
▶ simplehttpserver 
2021/01/11 21:40:48 Serving . on http://0.0.0.0:8000/...
2021/01/11 21:41:15 [::1]:50181 "GET / HTTP/1.1" 200 383
2021/01/11 21:41:15 [::1]:50181 "GET /favicon.ico HTTP/1.1" 404 19
```

# Thanks

simplehttpserver is made with 🖤 by the [projectdiscovery](https://projectdiscovery.io) team. Community contributions have made the project what it is. See the **[Thanks.md](https://github.com/projectdiscovery/simplehttpserver/blob/master/THANKS.md)** file for more details.
