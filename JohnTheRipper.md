# Update your System
```
sudo apt update && sudo apt upgrade -y
```

# Install JohnTheRipper and check installation
```
sudo apt install john -y
john --version
```

# Extract a Password Hash from /etc/shadow
```
sudo cat /etc/shadow
echo 'copied password ~ user:$6%randomsalt$hashedpassword' > hash.txt
```

![image](https://github.com/user-attachments/assets/2f53de57-0ef5-4e96-ab11-9000018810ef)

# Download rockyou.txt and move to a Standard Location
```
wget https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt
sudo mkdir -p /usr/share/wordlists/
sudo mv rockyou.txt /usr/share/wordlists

```

# Install clinfo and check GPU
```
#optional
sudo apt install clinfo
```

# Run John for password Cracking
```
john --wordlist=/usr/share/wordlists/rockyou.txt --fork=$(nproc) hash.txt
```

