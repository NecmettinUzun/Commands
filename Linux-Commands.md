# App Analysis
## Show Thread list
> jcmd <-PID-> Thread.print
## Thread dump and open it
> jmap -dump:format=b,file=/home/heap.bin <PID>
> 
> ./jhat -J-Xmx10240m -port 80 /home/heap.bin

# File Operation
## String update into the file
> sed -i 's/old_string/new_string/g' file
## Copy lines from file to another

# Grep-awk
> df -h | grep home
> > /dev/mapper/centos-home   46G  510M   45G   2% /home
> > 
> df -h | grep home | awk '{print $4}'
> > 45G

# Grep-cut
> df -h | grep home
> > /dev/mapper/centos-home   46G  510M   45G   2% /home
> 
> Getting between 39-42 characters
> 
> df -h | grep home | cut -c39-42
> > 45G
