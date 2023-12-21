# App Analysis
> ## Show Thread list
> jcmd <-PID-> Thread.print
> ## Thread dump and open it
> jmap -dump:format=b,file=/home/heap.bin <PID>
> 
> ./jhat -J-Xmx10240m -port 80 /home/heap.bin
> ## Thread CPU usage
> ps -p <PID> -L -o pid,tid,psr,pcpu
> 
> - command result will like this
> 
> 30186 38040  18  0.0
>
> - convert 30186 value to hex and search it in the thread dump
> ## Getting histogram
> jcmd <-PID-> GC.class_histogram > /root/histo.txt  


# File Operation
> ## String update into the file
> sed -i 's/old_string/new_string/g' file
> ## Find, Delete, List
>  - Delete files that is created 30 minute ago
> 
> find /home/test -type f -mmin +30 -exec rm -f {} \;
>
>  - List files that is created 20 days ago
>
> find . -name "*.gclog" -mtime +20 -exec ls -ltr {} \;
> ## Create large size file
> dd if=/dev/zero of=/var/lib/mysql/testfile.1.img bs=8000 count=280000
> ## File copy
> scp -r user@x.x.x.x:/home/test.jar .
> ## File permision definitions
> chmod u=rwx,g=rx,o=r myfile
> 
> chmod 754 myfile
> - 4 stands for "read",
> - 2 stands for "write",
> - 1 stands for "execute", and
> - 0 stands for "no permission."
>   
> So 7 is the combination of permissions 4+2+1 (read, write, and execute), 5 is 4+0+1 (read, no write, and execute), and 4 is 4+0+0 (read, no write, and no execute).


# Searching
> ## Grep-awk
> df -h | grep home
> > /dev/mapper/centos-home   46G  510M   45G   2% /home
> > 
> df -h | grep home | awk '{print $4}'
> > 45G

> ## Grep-cut
> df -h | grep home
> > /dev/mapper/centos-home   46G  510M   45G   2% /home
> 
> Getting between 39-42 characters
> 
> df -h | grep home | cut -c39-42
> > 45G

> ## Grep-before&after
> grep -A 1 -B 1 "serchedText"  entity.properties
>
> - B: before 1 line
> - A: after 1 line

 # Memory Usage
> ## Memory usage for all app
> ps -eo pmem,pid,pcpu,rss,vsize,args | sort -k 1 -r | head -10
