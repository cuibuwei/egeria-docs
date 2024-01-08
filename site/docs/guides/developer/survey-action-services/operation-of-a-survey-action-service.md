<!-- SPDX-License-Identifier: CC-BY-4.0 -->
<!-- Copyright Contributors to the Egeria project. -->

![Operation of an open discovery service](/guides/developer/open-discovery-services/open-discovery-service-operation.svg)
    
1. Each time an open discovery service runs, Egeria creates a discovery analysis report to describe the status and results of the open discovery service's execution.  The open discovery service is passed a [discovery context](/guides/developer/open-discovery-services/overview/#discovery-context) that provides access to metadata.
2. The *discovery context* is able to supply metadata about the asset and create a connector to the digital resource using the connection information linked to the asset.  The discovery service uses the connector to access the digital resource's contents in order to perform the analysis.
3. The discovery service creates *discovery annotations* to record the results of its analysis. It adds them to the discovery context which stores them in open metadata attached to the discovery analysis report.
4. The discovery annotations can be reviewed and commented on through an external stewardship process.  This means choices from, for example, a list of potential options proposed by the discovery services, can be verified and the best one selected by an individual expert.  The resulting choices are added to annotation reviews attached to the appropriate annotations.
5. The next time the open discovery service runs, a new discovery analysis report is created to link new attachments.  
6. The discovery context provides access to the existing attachments for that asset along with any annotation reviews.  The discovery services is able to link its new annotations to the existing annotations as an annotation extension.  This means that the stewards can see the history associated with the new information.




