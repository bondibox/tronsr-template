We will be building our primary cluster instance at the Linode data center in Atlanta Georgia, USA., where they offer an OC768 incoming network connection, with 40 Gbps in and 10 Gbps out. We believe that the incoming network connection will be critical for the Super Representative nodes.

Because the Tron Virtual Machine acts like one big symmetric multiprocessor cluster, we do not need a one-size-fits-all server instance, instead we will be building several server instances each with a specific task.

A Super Representative faces two technical responsibilities. The mission critical component is running a well protected Witness Node. Then you must make available lots of flops and storage for TVM the Tron Virtual Machine.

Our Primary cluster surrounds our Witness node with 6 Sentry nodes, which connect to the Witness via an IPSec tunnel. This cloaks the witness from the outside world, and allows it to advertise a private IP address. The 6 Sentry nodes act as the point of contact for the witness node, meaning a successful DDoS attack would have to discover and compromise all 6 Sentries. The Sentries will then be surrounded by unprotected Full Nodes which do the heavy lifting of the network. 8 of these nodes are configured to provide the most resources per dollar, and 4 are provisioned with 40/10 Gbps network connections for a total of more than 50 Gbps outbound bandwidth, since total bandwidth is the sum of all the nodes' guaranteed throughput.

Our primary deployment will provide **280 Cores + 1620 GB RAM + 23 TB SSD** for the Tron Virtual Machine:  

1x Witness Node $160 each  
6x Sentry Nodes $160 each  
2x High Mem High I/O Node $960 each  
2x High CPU High I/O Node $960 each  
8x Worker Nodes $320 each

$7520 + .02¢ per GB data transfer after the first 330 TB. For every .04¢ gain in TRX price we will add another cluster.




| Name | I/O High MEM |
|---|---|
| RAM | 	300 GB 
| CPU  | 	16 Cores
| SSD  | 	340 GB 
| Network  | 	40/10 Gbps 
| Transfer | 9 TB |
| Cost | 	$960 month 
| Purpose | High Memory / High bandwidth node | 


| Name | I/O High CPU |
|---|---|
| RAM |          192 GB  | 	
| CPU  |         32 Cores  | 	
| SSD  |         3.8 TB  | 	
| Network |      40/10 Gbps  | 	
| Transfer |  20 TB |
| Cost |         960 month |
| Purpose | High CPU / High bandwidth node |  


| Name |  SENTRY NODE & WITNESS NODE  | 
|---|---|
| RAM | 	          32 GB | 
| CPU  | 	          8 Cores  | 	
| SSD  | 	      	640 GB|  	
| Network  |          40/2 Gbps  | 	
| Transfer | 16 TB |
| Cost |      $160 month| 
| Purpose |   IPSec Tunneled Witness & Reverse Proxies  | 
         

             
| Name | WORKER NODE  |
|---|---|
| RAM | 	64 GB 
| CPU  | 	16 Cores
| SSD  | 	1280 GB 
| Network  | 	40/4 Gbps 
| Transfer | 20 TB |
| Cost | 	$320 month 
| Purpose |  Lowest Resource Cost | 


