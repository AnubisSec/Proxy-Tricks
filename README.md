# Proxy-Tricks
```Some tips about privoting with ssh and proxychains/nmap```



# First connect to pivot host with ssh credentials
```ssh -D <port> user@pivot-host```
  
# Then update proxychains.conf as needed depending on the port you used above
```vim /etc/proxychanins.conf```

# Finally, using nmap through proxychains requires the -sT flag since SYN method will not get through firewalls
```proxychains nmap -sT <host>```
