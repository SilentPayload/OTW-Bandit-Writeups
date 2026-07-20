# Bandit: Level 4 → Level 5

## 🎯 The Objective
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
## 🛠️ Commands used
- 'ls'
- 'cd'
- 'file'
- 'cat'

# Solution
ssh -p 2220 bandit4@bandit.labs.overthewire.org
i used the ls command to see what i have and i saw a directory named *inhere*, then i moved into the directory and saw a list of files named -file01 to file09 as shown below:

![Terminal output showing the file command identifying ASCII text](assets/bandit4-5.png)


* **Password: Redacted**

## Concept
**File Type Identification (Magic Numbers):** 
In Linux, file extensions (like `.txt` or `.png`) are just naming conventions and can easily be changed or omitted. To accurately determine what kind of data a file contains, the operating system looks at its **magic numbers**—specific byte signatures located in the file's header. The `file` command reads these headers to bypass misleading names and identify whether a file contains binary data, executable code, or plain ASCII text.
