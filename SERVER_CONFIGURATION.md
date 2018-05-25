The recommended configuration is an Amazon AWS x1.16xlarge with 25 Gbps network i/o but we have found a hosting service with a OC768 incoming network connection, offering 40 Gbps in and 10 Gbps out. We believe that the incoming network connection will be critical for the Super Representative nodes, and the outbound connection will be used more with the Full Nodes. Therefore we believe there exists the potential for this service to be superlative to the de facto standard.

ATLANTA DATA CENTER  
200 	GB RAM    
16 		CPU Cores        
2+		TB SSD Storage  
2		GB Swap  
40 		Gbps Network In    
10 		Gbps Network Out

Since AWS has a higher outbound network connection than our main node, we will also deploy Full nodes on AWS as data slaves.

Currently, we are researching the building of a cluster of server instances running in parallel for nearly unlimited resources, as well as adding docker, kubernetes, and hadoop replication and deployment services.

