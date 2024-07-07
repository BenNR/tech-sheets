
# List all processes
htop -t

# List filesystem
ls -la

# Create user
sudo useradd -m -s /bin/bash new_username
sudo adduser john



# List all groups
cat /etc/group
=> adm:x:4:syslog,ben == groupname:password:groupId:membersList

#Add user to group
sudo usermod -aG groupname username


# List groups of user
groups <user>


# Change ownership 

sudo chown username:groupname filename

#Change group ownership recursively of a directory
sudo chgrp -R groupname directory
sudo chown -R user:group directory


# Chamge permissions of owners

rwx rwx rwx - <owner> <group> <other>

chmod[u/g/o][+/-/=][r/w/x] [file]

chmod u=rwx,g=rw,o=r test

chmod 640 test

https://chmod-calculator.com/


# Identify current user group memberships
whoami
id