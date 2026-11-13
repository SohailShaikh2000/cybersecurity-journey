# OverTheWire: Bandit Walkthrough & Notes

## Level 0 -> Level 1

* **Concept:** Connecting via SSH on a non-standard port.
* **Commands Used:**
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
cat readme
```

## Level 1 -> Level 2

* **Concept:** Password located in a file called `-`
* **Commands Used:**
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
cat ./-
```

## Level 2 -> Level 3

* **Concept:** Password stored in a file called `--spaces in this filename--`
* **Commands Used:**
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
cat -- "--spaces in this filename--"
```

## Level 3 -> Level 4

* **Concept:** Password stored in a hidden file
* **Commands Used:**
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
cd inhere
ls -a
cat ...Hiding-From-You
```

## Level 4 -> Level 5

* **Concept:** Password for the next level is stored in the only human-readable file in the `inhere` directory
* **Commands Used:**
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
cd inhere
ls
file ./*    # Look for ASCII text
cat ./-file07
```

## Level 5 -> Level 6

* **Concept:** Password is stored in a file somewhere under the `inhere` directory (human-readable, 1033 bytes in size, not executable)
* **Commands Used:**
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
cd inhere
ls
find . -size 1033c ! -executable
cat #path to found file
```
