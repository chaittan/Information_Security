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

# Install Wordlists Package and then Extract It
```
sudo apt install wordlists -y
gunzip /usr/share/wordlists/rockyou.txt.gz

#Check Installation
ls -lh /usr/share/wordlists/rockyou.txt
```
