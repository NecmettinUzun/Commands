# App Analysis
## Show Thread list
> jcmd <-PID-> Thread.print

# File Operation
## String update into the file
> sed -i 's/old_string/new_string/g' file

# Grep-awk
> df -h | grep home
> > /dev/mapper/centos-home   46G  510M   45G   2% /home
> df -h | grep home | awk '{print $4}'
> > 45G
