```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall

    Attacker->>BotNet: Command to start attack
    BotNet->>WebServer: Send flood of requests
    WebServer->>Firewall: Detect unusual traffic
    Firewall-->>WebServer: Analyze and block IPs
    Firewall-->>BotNet: Block malicious IPs
    BotNet-->>Attacker: Report blocked
    BotNet->>WebServer: Continue sending requests
    WebServer->>Firewall: Request more defense
    Firewall-->>BotNet: Initiate DDoS mitigation

### Step 4: Write the Documentation
Below the diagram, explain the steps in the sequence:

```markdown
### Sequence Diagram Explanation

1. **Attacker** sends a command to the **BotNet** to start the DDoS attack.
2. The **BotNet** sends a massive amount of requests to the **WebServer**, overwhelming its resources.
3. The **WebServer** detects abnormal traffic and forwards it to the **Firewall** for analysis.
4. The **Firewall** analyzes the traffic and identifies the IP addresses sending the flood of requests, blocking them.
5. The **BotNet** notifies the **Attacker** that some IPs have been blocked, but it continues sending more requests to the **WebServer**.
6. The **WebServer**, unable to handle the ongoing attack, asks the **Firewall** for additional defense.
7. The **Firewall** implements more advanced DDoS mitigation strategies to stop the attack.
