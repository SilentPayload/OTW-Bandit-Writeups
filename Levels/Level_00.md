# Bandit: Level 0

## 🎯 The Objective
Connect to the server via SSH using the provided credentials.

## 🛠️ Connectivity Check
```bash
# Verifying host reachability
ping bandit.labs.overthewire.org and it was active i also got an ip address
- 51.20.162.29
# Solution
ssh -p 2220 bandit0@51.20.162.29
- I then input the password given and i solved the level
