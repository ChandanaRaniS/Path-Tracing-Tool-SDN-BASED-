# SDN-Based Path Tracing Tool

**Name:** Chandana Rani S
**SRN:** PES2UG24AM044

---

## Project Overview

This project implements a Software Defined Networking (SDN) based Path Tracing Tool using the Ryu controller and Mininet emulator. The system monitors packet flow and displays the path taken by packets across switches in real time.

---

## Objective

* To understand SDN architecture
* To implement a controller using Ryu
* To trace packet paths dynamically
* To analyze network behavior under normal and failure conditions

---

## SDN Architecture

In Software Defined Networking:

* The control plane is managed by the Ryu controller
* The data plane is handled by switches
* The controller installs flow rules dynamically based on network events

---

## Mininet Topology

A linear topology is used with:

* 3 Hosts: h1, h2, h3
* 3 Switches: s1, s2, s3

Connections:
h1 — s1 — s2 — s3 — h3
              |
              h2

---

## Requirements

* Ubuntu or Linux environment
* Mininet
* Ryu Controller
* Python 3

---

## Controller Implementation

The controller is implemented using the Ryu framework in Python. It performs the following:

* Handles packet_in events
* Learns MAC addresses
* Determines forwarding decisions
* Logs switch traversal for path tracing

---

## Flow Rule Management

Flow rules are dynamically installed using match-action logic:

* Match fields: source MAC, destination MAC
* Actions: forward to appropriate port

---

## Functionality Implementation

The system performs:

* Packet forwarding
* MAC learning
* Path tracing through switches
* Dynamic flow rule installation

Example output:
Switch s1 → s2 → s3

---

## Performance Evaluation

### Connectivity Test

pingall
Result: 0% packet loss

### Latency Test

h1 ping -c 3 h3

### Throughput Test

iperf h1 h3

### Failure Scenario

link s1 s2 down

Result:
Partial packet loss observed

Recovery:
link s1 s2 up

Result:
Network restored successfully

---

## Python Script

path_tracing.py

---

## Demo Screenshots

(Add your screenshots here)

---

## GitHub Repository

https://github.com/ChandanaRaniS/Path-Tracing-Tool-SDN-BASED-

---

## Conclusion

This project demonstrates SDN-based path tracing using the Ryu controller and Mininet. The controller dynamically installs flow rules and provides visibility into packet movement across switches. The system performs correctly under both normal and failure conditions.
