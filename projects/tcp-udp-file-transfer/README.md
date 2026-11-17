# TCP / UDP File Transfer

**Source code:** [file-transfer-udp-tcp](https://github.com/ST3PAN0V/file-transfer-udp-tcp)  
**Context:** Technical assessment  
**Focus:** Sockets · Network protocols · Verification scripts

A Python client-server exercise implementing file transfers over TCP and UDP. Each protocol has its own implementation branch.

## Implementation

| Branch | Contents |
| :--- | :--- |
| [tcp](https://github.com/ST3PAN0V/file-transfer-udp-tcp/tree/tcp) | A server sends file data to a connected client over a TCP socket. |
| [udp](https://github.com/ST3PAN0V/file-transfer-udp-tcp/tree/udp) | A server receives a client request and sends file data as UDP datagrams. |

Both branches contain separate client/server programs and Bash test scripts. The TCP script creates a random file, starts the programs, and compares the received contents with the original.

## Engineering focus

- Establishing connections and exchanging data through Python sockets.
- Understanding the different delivery semantics of TCP and UDP.
- Coordinating client/server processes from Bash.
- Checking transferred content independently of program log messages.

These are small assessment implementations. The UDP version does not implement acknowledgements or retransmission, and the servers are intended for a single transfer per run.

## Stack

**Python · socket · TCP · UDP · Bash**

[Read setup and usage instructions](https://github.com/ST3PAN0V/file-transfer-udp-tcp#readme)

[← Back to portfolio](../../README.md)
