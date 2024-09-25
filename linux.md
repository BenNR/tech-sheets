
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

# Add user to group => Only effect after relogin
sudo usermod -aG groupname username


# List groups of user
groups <user>/blank


# Change ownership 

sudo chown username:groupname filename

#Change group ownership recursively of a directory
sudo chgrp -R groupname directory
sudo chown -R user:group directory


# Chamge permissions of owners

rwx rwx rwx - <owner> <group> <other>

chmod[u/g/o][+/-/=][r/w/x] [file]

chmod u=rwx,g=rw,o=r test
chmod +x app.py => Applies to r/g/o

chmod 640 test

https://chmod-calculator.com/


# Identify current user group memberships
whoami
id


# Sudo 
sudo cat /etc/sudoers

# List all things user can do using sudo
sudo -l

# Sudo editing
visudo => Syntax error = What now? e (edit)

# User cam access apt and rm  without pw request
user    ALL=(ALL:ALL) NOPASSWD: /usr/bin/apt, /usr/bin/rm
%user => group


# Execution requirements
binary require execution privileges (already compiled)
non compiled code just need read on the file (eg. app.py) and execution on the interpreter
shebang defines interpreter #!/usr/bin/python3

apps can be run ./app.py if shebang present x on file required
if app run python3 app.py only read on file and execute on interpreter


# PATH
echo $PATH => path to where commands are located eg. ls, rm ...

evaluated in order first found /bin/ls:/root/ls 

which <command> => Finds where executable is located


# Modifiy bash for individual users
~/.bashrc


# List Memory Usage Cached Memory
free -wh

# List IOPS
apt install sysstat

iostat -dxm sda

# List size
du -sh <directory>
