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
