# Using John the Ripper

## Update your System
```
sudo apt update && sudo apt upgrade -y
```

## Install JohnTheRipper and check installation
```
sudo apt install john -y
john --version
```

## Extract a Password Hash from /etc/shadow
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
nproc identifies the number of cpu cores and forks those many processes to make the cracking faster
![image](https://github.com/user-attachments/assets/ca0c88a5-0770-4cb9-8355-6db1f37a30e7)

You can check the status by pressing almost any key except (q) [for quitting]
![image](https://github.com/user-attachments/assets/9078f4b6-80ce-497b-aacf-4180a3a5295b)


# Use Keyboard interrupt to stop once cracked 
```
john --show hash.txt
```

![image](https://github.com/user-attachments/assets/5cb995c0-c535-4569-9ecc-01a9e37d91ac)

# Use HashCat to crack passwords

## To be updated

# Task 3
```
# create a new user
sudo adduser chaitanya
sudo cat /etc/shadow
sudo cat /etc/passwd

# change user on terminal
su chaitanya

# check the logged in user
whoami

exit

# change user's home directory
sudo usermod -d / chaitanya
```

```
sudo addgroup groupname

sudo cat /etc/group
```
![image](https://github.com/user-attachments/assets/4f15c447-4bde-46ae-b39d-ff0ede66d8f5)

```

```
#add user to a group
sudo adduser username groupname

#append user to another groups
sudo usermod -aG groupname username

#change users primary group
sudo usermod -g groupname username
```
![image](https://github.com/user-attachments/assets/fdab95d1-5d59-4f34-b92e-c04e4063f166)


