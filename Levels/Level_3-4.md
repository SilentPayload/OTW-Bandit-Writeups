# Bandit: Level 3 → Level 4

## 🎯 The Objective
The password for the next level is stored in a hidden file in the inhere directory.
## 🛠️ Commands used
ls
la -la
cd
cat .

# Solution
ssh -p 2220 bandit3@bandit.labs.overthewire.org

Ran the command ls -la to list all the files and i saw a directory called inhere. I then changed directory using cd. When in the inhere directory, i ran the command ls and saw nothing; i then ran the command ls -la and saw the hidden file. i can ran the command cat ...Hidden file and got the password.
* **Password: Redacted**