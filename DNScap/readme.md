# DNScap

```
from scapy.all import *

p=rdpcap('dnscap.pcap') 

x=""
y=""
temp=""

for i in p:
    if i in p[DNSQR] and i not in p[DNSRR]:   # To remove all the response packets from the requested packets we are using this condition.
 
        x=(i[DNSQR].qname)[18:-18]  # Here we are removing starting 18 bits of information since they are just scrap and the last 18 bits are .skulllabsec.org
        x=x.replace('.','')
        x=x.decode('hex') # Decode from Hex.
        if(x==temp): # To eliminate the retransmissions we check the current data with the previous data.
            continue  # If same then move to next iteration.
        y+=x
        temp=x

f=open('final.png','w')
f.write(y[95:]) # First few contains just some description.
f.close()
```

