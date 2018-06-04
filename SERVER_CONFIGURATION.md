We will be building our primary cluster instance at the Linode data center in Atlanta Georgia, USA., where they offer an OC768 incoming network connection, with 40 Gbps in and 10 Gbps out. We believe that the incoming network connection will be critical for the Super Representative nodes.

Because the Tron Virtual Machine acts like one big symmetric multiprocessor cluster, we do not need a one-size-fits-all server instance, instead we will be building several server instances each with a specific task.


It should be noted that since each node has a guaranteed throughput network connection, total bandwidth is the sum of all the nodes output.

Our primary server cluster Instance will provide **248 Cores + 1292 GB RAM + 24 TB SSD** for the Tron Virtual Machine:  

1x Witness Node $160 each  
6x Sentry Node $160 each  
1x High Mem High I/O NODE $960 each  
1x High CPU High I/O Node $960 each  
9x Worker Nodes $320 each

                                               
$5920 + .02¢ per GB data transfer after the first 320 TB.  
Estimated monthly expense $10,000




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
| Purpose |   IPSec Tunneled Witness & Witness Border Nodes  | 
         

             
| Name | WORKER NODE  |
|---|---|
| RAM | 	64 GB 
| CPU  | 	16 Cores
| SSD  | 	1280 GB 
| Network  | 	40/4 Gbps 
| Transfer | 20 TB |
| Cost | 	$320 month 
| Purpose |  Lowest Resource Cost | 


