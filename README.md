# 🌐 NetPractice

*This project has been created as part of the 42 curriculum by xviladri.*

## 📝 Description

NetPractice is a general practical exercise designed to introduce the basics of computer networking. The main goal is to understand how to configure IP addresses, connect devices through a router, and understand the role of a gateway within a network.

The project consists of solving 10 levels of simulated small-scale networks. In each level, a non-functioning network diagram is presented, and the objective is to fix the configuration (IPs, subnet masks, and routing tables) to achieve specific communication goals between hosts and the internet.

### 🧠 Core Learnings & Problem-Solving

Throughout this project, I developed a deep understanding of network logic rather than just trial and error:

* **Subnetting (Cutting the pie):** I learned how to divide a large `/24` network into smaller, isolated networks (e.g., using a `/26` mask to create 4 subnets of 64 IPs) to avoid routing conflicts.
* **The Golden Rule of Routers:** A router's primary job is to connect different networks. Two interfaces on the same router can never belong to the same subnet, or the routing table will fail.
* **Network and Broadcast Addresses:** I learned why the first IP of a subnet block is reserved for the network identifier, and the last IP is reserved for the Broadcast address (meaning they cannot be assigned to individual hosts).
* **Route Aggregation (Supernetting):** Grouping smaller subnets (like `/28`) into a single larger routing rule (like `/26`) to simplify routing tables when communicating with the outside Internet.
* **Default Routes:** Understanding that `0.0.0.0/0` (or `default`) acts as the "exit door" for any packet destined for an unknown IP address.

---

## 🚀 Instructions

To run the training interface and test the network configurations:

* **Note:** If the script fails, you can run `python3 -m http.server 49242` and navigate to `http://localhost:49242` in your browser.
* On the web interface, enter your 42 intranet login (`xviladri`) so the Moulinette can validate your specific configuration.
* Solve the levels by modifying the unshaded fields until the network functions properly.
* **Exporting Configurations:** Before moving to the next level, you must export your working configuration by clicking the **[Get my config]** button.

---

## 📦 Submission Requirements

* For the final evaluation, 10 exported configuration files (one per level) must be placed directly at the root of the Git repository.
* During the defense, I will have to successfully solve three random levels without the use of external tools. Only a simple calculator like `bc` is allowed.
  
---

## 📚 Resources

To successfully complete this project, the following classic networking concepts were studied and applied:

* TCP/IP addressing
* Subnet masks (CIDR notation and binary calculation)
* Default gateways
* Routers and switches
* OSI layers
* Routing tables and Forwarding

### 🤖 Use of AI

Following the 42 AI Instructions, Artificial Intelligence (such as Gemini AI) was used purely as a tutor and sparring partner to understand the mathematical logic behind networking. AI was specifically used to:

* Explain the binary logic behind Subnetting (how "stealing bits" from a `/24` creates a `/26` mask).
* Help troubleshoot specific routing logic errors (e.g., explaining why a `/32` mask creates a "No reverse way" error and how to calculate the correct base network address for a `/25` mask).
* Clarify the conceptual difference between a local Gateway and an external ISP Router.

*No AI was used to generate direct answers or files; it was utilized strictly to build the computational thinking and domain-specific knowledge required to solve the levels independently and explain them during the peer evaluation.*
