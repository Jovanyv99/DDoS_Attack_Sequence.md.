# DDoS_Attack_Sequence.md.

sequenceDiagram
participant Attacker
participant BotNet as Compromised Bots
participant WebServer as Targeted Web Server
participant Firewall as Firewall/Defense System

Attacker->>BotNet: Issue attack instructions
BotNet->>WebServer: Flood with massive requests
WebServer-->>Firewall: Alert: Unusual traffic detected
Firewall->>WebServer: Analyze traffic patterns
Firewall->>BotNet: Block IP addresses of bots
BotNet->>WebServer: Continue sending requests (adjust IPs)
Firewall->>Firewall: Update filtering rules
Firewall->>Attacker: Attempt traceback
WebServer->>Firewall: Mitigation measures initiated


# DDoS Attack Sequence Diagram

## Description

This diagram illustrates the flow of a Distributed Denial of Service (DDoS) attack on a web server, involving multiple participants:

1. **Attacker**: The initiator of the attack who commands a network of compromised devices (BotNet).
2. **BotNet**: A collection of malware-infected devices controlled by the attacker, used to send massive traffic to the web server.
3. **WebServer**: The target of the attack, overwhelmed by the flood of requests, causing a denial of service to legitimate users.
4. **Firewall**: The defense system in place to identify and mitigate malicious traffic patterns, ensuring service availability.

## Sequence of Events

1. **Attack Initiation**:
   - The attacker sends instructions to the BotNet, activating the devices to begin flooding the web server with excessive requests.

2. **Flooding the Target**:
   - The BotNet devices send high volumes of traffic simultaneously, consuming the server's resources.

3. **Detection and Alerts**:
   - The web server detects unusual traffic patterns and notifies the firewall about the ongoing attack.

4. **Traffic Analysis**:
   - The firewall analyzes the incoming traffic to identify malicious requests and block the corresponding IP addresses.

5. **Dynamic Adjustments**:
   - The BotNet adapts by changing IP addresses to bypass the firewall, while the firewall updates its rules to counteract the new attack patterns.

6. **Traceback Attempts**:
   - The firewall may attempt to trace the source of the attack back to the attacker for further investigation.

7. **Mitigation Measures**:
   - The web server, with assistance from the firewall, deploys additional measures like rate limiting, load balancing, or blackholing malicious traffic to maintain service for legitimate users.

## Purpose

This description complements the visual Mermaid diagram, ensuring clarity about the flow of events in a typical DDoS attack, the roles of each participant, and the defensive mechanisms employed.
