# GoNetworkProfiler  

GoNetworkProfiler is a lightweight, real-time network monitoring tool written in Go. It uses packet sniffing and protocol parsing to provide insights into network activity. The tool allows users to list available network interfaces and monitor live traffic on a specified interface.

---

## Features
- **List Network Interfaces**: Displays all available network interfaces on the system with their descriptions.
- **Live Packet Capture**: Captures and displays raw network packets in real time.
- **Promiscuous Mode Support**: Enables monitoring of all network traffic on a given interface.
- **Easy-to-Use**: Simple, modular functions for listing devices and sniffing packets.

---

## Getting Started

### Prerequisites
1. **Go (Golang)**: Ensure you have Go installed on your system. Download it [here](https://golang.org/dl/).
2. **libpcap**: Install the `libpcap` library on your system:
   - **Linux**: Use your package manager (e.g., `sudo apt install libpcap-dev` on Ubuntu).
   - **MacOS**: Use Homebrew (`brew install libpcap`).
   - **Windows**: Install WinPcap or Npcap.

---

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/upanshu21/GoNetworkProfiler.git
   cd GoNetworkProfiler

```go mod tidy
```

List Available Interfaces

```
go run main.go list
```

Start Packet Sniffing

```
go run main.go sniff -i <interface_name>
```

Example Output

```
$ go run main.go list
Name: eth0, Description: Ethernet Interface
Name: wlan0, Description: Wireless Interface
Name: lo, Description: Loopback Interface
```

Sniffing Packets

```
$ go run main.go sniff -i eth0
Packet: Ethernet {Contents=[..] Payload=[..]}
Packet: IPv4 {Contents=[..] Payload=[..]}
Packet: TCP {Contents=[..] Payload=[..]}
```

### License
This project is licensed under the MIT License. See the LICENSE file for details.
