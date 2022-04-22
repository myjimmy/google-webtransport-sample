WebTransport Sample
===
See https://googlechrome.github.io/samples/webtransport/client.html for a live demo of the client.

There's code for a sample local server at https://github.com/GoogleChrome/samples/blob/gh-pages/webtransport/webtransport_server.py

Learn more at https://chromestatus.com/feature/4854144902889472


Installation
============

- Install python3.9

```
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt install python3.9 python3.9-venv
```
- Install the dependencies

```
$ python3.9 -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

- Run webtransport server

```
$ python webtransport_server.py certs/ssl_cert.pem certs/ssl_key.pem
```

- Run Chrome with the following parameters.
```
$ google-chrome --enable-experimental-web-platform-features --origin-to-force-quic-on=localhost:4433 --ignore-certificate-errors-spki-list=BSQJ0jkQ7wwhR7KvPZ+DSNk2XTZ/MS6xCbo9qu++VdQ=
```
