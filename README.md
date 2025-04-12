**Comprehensive Linux Administration Command List**

---

### 1. **System Information**

- Display system information:
  ```bash
  uname -a
  ```
- Display kernel version:
  ```bash
  uname -r
  ```
- Check system uptime:
  ```bash
  uptime
  ```
- Show detailed system information:
  ```bash
  lsb_release -a
  ```
- Display CPU information:
  ```bash
  cat /proc/cpuinfo
  ```
- Display memory information:
  ```bash
  cat /proc/meminfo
  free -h
  ```

---

### 2. **File and Directory Operations**

- List files in a directory:
  ```bash
  ls -l
  ls -a
  ```
- Create a directory:
  ```bash
  mkdir new_directory
  ```
- Remove a directory:
  ```bash
  rmdir empty_directory
  ```
- Create a file:
  ```bash
  touch newfile.txt
  ```
- View file content:
  ```bash
  cat file.txt
  less file.txt
  head file.txt
  tail file.txt
  ```
- Copy files:
  ```bash
  cp source.txt destination.txt
  ```
- Move or rename files:
  ```bash
  mv oldname.txt newname.txt
  ```
- Delete files:
  ```bash
  rm file.txt
  ```
- Find files:
  ```bash
  find /path/to/search -name "filename"
  ```

---

### 3. **User Management**

- Create a new user:
  ```bash
  sudo adduser newuser
  ```
- Delete a user:
  ```bash
  sudo deluser username
  ```
- Change a user password:
  ```bash
  passwd username
  ```
- Switch user:
  ```bash
  su - username
  ```
- View current user:
  ```bash
  whoami
  ```

---

### 4. **Group Management**

- Create a new group:
  ```bash
  sudo groupadd newgroup
  ```
- Add a user to a group:
  ```bash
  sudo usermod -aG groupname username
  ```
- Remove a user from a group:
  ```bash
  sudo gpasswd -d username groupname
  ```
- View groups of a user:
  ```bash
  groups username
  ```

---

### 5. **File Permissions**

- View file permissions:
  ```bash
  ls -l file.txt
  ```
- Change file permissions:
  ```bash
  chmod 755 file.txt
  ```
- Change file ownership:
  ```bash
  sudo chown username:groupname file.txt
  ```
- Add execute permission:
  ```bash
  chmod +x script.sh
  ```

---

### 6. **Disk Management**

- Check disk usage:
  ```bash
  df -h
  ```
- Check directory size:
  ```bash
  du -sh /path/to/directory
  ```
- Create a new partition:
  ```bash
  sudo fdisk /dev/sdX
  ```
- Format a partition:
  ```bash
  sudo mkfs.ext4 /dev/sdX1
  ```
- Mount a partition:
  ```bash
  sudo mount /dev/sdX1 /mnt
  ```
- Unmount a partition:
  ```bash
  sudo umount /mnt
  ```

---

### 7. **Package Management**

- For Debian-based systems (e.g., Ubuntu):
  ```bash
  sudo apt update
  sudo apt upgrade
  sudo apt install package-name
  sudo apt remove package-name
  sudo apt autoremove
  ```
- For Red Hat-based systems (e.g., CentOS):
  ```bash
  sudo yum update
  sudo yum install package-name
  sudo yum remove package-name
  ```

---

### 8. **Process Management**

- View running processes:
  ```bash
  ps aux
  ```
- Search for a process by name:
  ```bash
  ps aux | grep process_name
  ```
- Kill a process by PID:
  ```bash
  kill -9 PID
  ```
- Monitor system performance:
  ```bash
  top
  htop
  ```
- View active processes with tree structure:
  ```bash
  pstree
  ```

---

### 9. **Networking**

- View IP configuration:
  ```bash
  ip addr
  ```
- Test network connectivity:
  ```bash
  ping -c 4 google.com
  ```
- View open ports:
  ```bash
  sudo netstat -tuln
  ```
- Test port connectivity:
  ```bash
  telnet hostname port
  ```
- Download a file:
  ```bash
  wget https://example.com/file
  ```

---

### 10. **Logs and Monitoring**

- View system logs:
  ```bash
  sudo tail -f /var/log/syslog
  ```
- View boot logs:
  ```bash
  dmesg
  ```
- View journal logs:
  ```bash
  sudo journalctl -xe
  ```

---

### 11. **Cron Jobs**

- Edit cron jobs:
  ```bash
  crontab -e
  ```
- View cron jobs:
  ```bash
  crontab -l
  ```
- Add a cron job (run script.sh daily at 2 AM):
  ```bash
  0 2 * * * /path/to/script.sh
  ```

---

### 12. **Backup and Restore**

- Backup a directory:
  ```bash
  tar -cvzf backup.tar.gz /path/to/directory
  ```
- Restore a directory:
  ```bash
  tar -xvzf backup.tar.gz
  ```

---

### 13. **Firewall Management**

- Check UFW status (Ubuntu):
  ```bash
  sudo ufw status
  ```
- Allow a port:
  ```bash
  sudo ufw allow 22
  ```
- Deny a port:
  ```bash
  sudo ufw deny 80
  ```
- Reload UFW:
  ```bash
  sudo ufw reload
  ```

---

### 14. **SSH Configuration**

- Generate SSH keys:
  ```bash
  ssh-keygen -t rsa
  ```
- Copy SSH key to remote server:
  ```bash
  ssh-copy-id user@remote_host
  ```
- Connect to a remote server:
  ```bash
  ssh user@remote_host
  ```

---

### 15. **Shell Scripting Basics**

- Create and run a shell script:
  ```bash
  echo -e '#!/bin/bash\necho "Hello, Linux!"' > script.sh
  chmod +x script.sh
  ./script.sh
  ```
- Run a loop in a script:
  ```bash
  for i in {1..5}; do echo "Number $i"; done
  ```

---

This is a broad list of commands and practices.

