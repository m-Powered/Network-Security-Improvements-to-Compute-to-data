## Ocean Protocol - Ocean DAO (Round 7) Local Network Egress Traffic Improvements to the Kubernetes configuration file for Compute-to-data
Improve the Kubernetes configuration to prevent all network egress traffic from the pod which contains the algorithm.
------

It will be the case that in a [compute-to-data](https://docs.oceanprotocol.com/tutorials/compute-to-data-algorithms/ "Ocean Protocol - Writing Algorithms for Compute to Data") (C2D) job, the data set publisher and the algorithm publisher will be separate entities and unknown to each other. The data set publisher has to trust that the algorithm won't steal the entire data set. The algorithm could accomplish this by simply copying the inputs folder to the outputs folder. To prevent this, the data set publisher could only allow trusted algorithms and vet them by potentially reviewing the code, and running the algorithm and analyzing the output.

It would still be easy for an algorithm to steal the data set by uploading it to a file server. To prevent this, we would change the Kubernetes configuration to prevent all network egress traffic from the pod which contains the algorithm and improve security. This will have a positive effect on C2D adoption.

This [github issue](https://github.com/oceanprotocol/multi-repo-issue/issues/90#issuecomment-804264134/ "allowNetworkAccess: boolean - if algo pod has network access during compute (not implemented yet in C2D)") states that the **allowNetworkAccess** is not yet implemented, but we believe this is imperative to C2D's success and adoption and that is why we are applying for an Ocean DOA (Round 7) and creating an Open Source repository where all other Ocean Developers can integrate into their projects and/or use as reference.

**There will be two deliverables for the Ocean DAO (Round 7)**

**Milestone #1**
A public repository will be made to these Ocean components: allowNetworkAccess: boolean - if algo pod has network access during compute (not implemented yet in C2D) as per this [GitHub issue](https://github.com/oceanprotocol/multi-repo-issue/issues/90#issuecomment-804264134/ "allowNetworkAccess: boolean - if algo pod has network access during compute (not implemented yet in C2D)") to help other development teams implement tighter security protocols.
*Expected Completion Date: July 19, 2021*

## Update: Status - Completed Milestone 1 ##
The code that we published to fix **allowNetworkAccess** and complete **Milestone #1** can be found [here](https://github.com/mPowered-io/operator-engine/ "allowNetworkAccess")
