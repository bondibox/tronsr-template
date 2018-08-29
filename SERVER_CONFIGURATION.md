A witness node is more than just a block producer. It also provides CPU flops, memory, and storage for the Tron Virtual Machine (TVM).

A Super Representative faces a two-pronged technical responsibility: Make resources available while protecting the Witness node providing those resources.

Our primary witness cluster is at the Linode data center in Atlanta Georgia, USA., where they offer an OC768 incoming network connection, with 40 Gbps in and up to 12 Gbps out. Too many witness nodes are using Alibaba, Google and AWS hosting services. An outage at one or all could be catastrophic to the Tron network. Therefore we have chosen a reliable alternative to these other providers.

Our Primary cluster surrounds our Witness node with 5 Sentry nodes, which connect to the Witness via an IPSec tunnel. This cloaks the witness from the outside world, and allows it to advertise a private IP address. The Sentry nodes act as the point of contact for the witness node, meaning a successful DDoS attack would have to discover and compromise all 5 Sentries. 

Currently we are starting with the following setup:

1 Primary Witness Node   
1 Backup Witness Node 
5 Full Nodes

Our next technical expansion will be to purchase a primary witness 128 core server with 1.5 TB of RAM, and colocate it along with 5 full nodes in Louisville KY on Flexential's 100 GbPS backbone.


| Witness Node |
|---|---|
| RAM |          192 GB  | 	
| CPU  |         32 Cores  | 	
| SSD  |         3.8 TB  | 	
| Network |      40/12 Gbps  | 	
| Transfer |  20 TB |
| Cost |         $960 month |
| Purpose | Block Production |  


| Full Nodes |  
|---|---|  
| RAM | 	64 GB  
| CPU  | 	16 Cores  
| SSD  | 	1280 GB  
| Network  | 	40/4 Gbps  
| Transfer | 20 TB |  
| Cost | 	$320 month   
| Purpose |  Protect Block Producer | 





