A witness node is more than just a block producer. It also provides CPU flops, memory, and storage for the Tron Virtual Machine (TVM).

A Super Representative faces a two-pronged technical responsibility: Make resources available while protecting the Witness node providing those resources.

Our primary witness cluster is at the Linode data center in Atlanta Georgia, USA., where they offer an OC768 incoming network connection, with 40 Gbps in and up to 12 Gbps out. Too many witness nodes are using Alibaba, Google and AWS hosting services. An outage at one or all could be catastrophic to the Tron network. Therefore we have chosen a reliable alternative to these other providers.

Our Primary cluster surrounds our Witness node with 3 Sentry nodes, which connect to the Witness via IPSec tunnels. This cloaks the witness from the outside world, and allows it to advertise a private IP address. The Sentry nodes act as the point of contact for the witness node, meaning a successful DDoS attack would have to discover and compromise all 3 Sentries. 

Currently we are starting with the following setup:

| Witness Node |
|---|---|
| RAM |          192 GB  | 	
| CPU  |         32 Cores  | 	
| SSD  |         3.8 TB  | 	
| Network |      40/12 Gbps  | 	
| Transfer |  20 TB |
| Cost |         $960 month |
| Purpose | Block Production |
| Benchmark | 7.3 maxTimeRatio |


| Full Nodes |  
|---|---|  
| RAM | 	64 GB  
| CPU  | 	16 Cores  
| SSD  | 	1280 GB  
| Network  | 	40/4 Gbps  
| Transfer | 20 TB |  
| Cost | 	$320 month   
| Purpose |  Protect Block Producer | 


Our benchmark tests have shown that the performance bottleneck is not CPU or RAM, but disk i/o. In other words it doesn't matter how much resources have been provisioned for the VM, if it is on a busy server with several high traffic VM instances there will be a disk queue that slows performance. In testing 16 core vs. 32 core VMs, the 32 core instance did not always perform better, and in fact usually did not. 

Therefore, for the rollout of the Tron Virtual Machine we will have a bare metal server with a 10 Gbps unmetered connection. Initially this machine will run a hypervisor and several VMs, each with its own 15k rpm SAS drive. The VM running the witness node will have 2 SAS drives in a RAID 0 configuration to optimize read functions, with 24 dedicated cores and 96 GB dedicated RAM.

Based on performance needs, our next step is to deploy a second server at the same location with higher RAM and CPU specs, and SSD storage.

Eventually our deployment will consist of a catalyst switch and 4 x 10 Gbps connections, using routing protocols to aggregate the bandwidth to the primary server which will also have 4 x 10 Gbps network cards.


