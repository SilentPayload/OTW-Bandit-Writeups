# Bandit Level 0 → Level 1

## 🎯 The Objective
Connect to the server via SSH as `bandit0` and locate the password for the next level (`bandit1`) hidden in the home directory.

## 🛠️ Commands Used
- `ssh`: Secure Shell for connecting to the remote server.
- `ls`: List files in the current directory.
- `cat`: Read the contents of a file.

## 📝 The Solution
1. Connect to the host on the specified port:
   ```bash
   `ssh -p 2220 bandit0@bandit.labs.overthewire.org` 

### Part 2: The "Mistake" Breakdown (Why you hit a wall)

You looked at the `sshd_config` file and got confused because i was thinking like a **System Administrator**, but the game requires you to think like an **Attacker**.



**My Mistake:** I was already logged into `bandit0` and tried to "become" `bandit1` from inside the server. 

**The Lesson:**
1.  **Server-Side vs. Client-Side:** I was looking at the *server's* configuration. The server is configured to prevent "lateral movement" (hopping from one user to another without logging out). This is a security feature! You *want* the server to be configured that way to keep users isolated.
2.  **The "Attacker" Perspective:** In a CTF/Wargame, you aren't an admin. You are an external user. You don't have the authority to modify the server's rules—you have to play by them. 
3.  **The "Ah-ha" Moment:** When I exit `bandit0` and reconnect as `bandit1`, i am effectively "re-attacking" the server with a new set of credentials. That is exactly how real-world authentication bypasses or credential-based attacks work.
