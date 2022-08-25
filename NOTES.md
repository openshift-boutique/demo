 ## Worklog

 The Microservices Demo provided by Google is a good starting base for a multifunction SaaS.

 The comments from the last pull request in it's previous repo loaction is listed below for documentation:

 ---
 PR: Service split 1

 Background
 The base repository was written by Google and was designed to have all of the services within one namespace. Additionally, while the proje
 Due to the enhanced security in OpenShift, and the want to segment roles and responsibilities for the microservices, we forked the origina

 Fixes
 Segmented the microservices into the following namespaces:

 Client1:

 adservice
 rediscart
 frontend
 Boutique-Ops

 cartservice
 checkoutservice
 loadgenerator
 productcatalog
 recommendationservice
 shippingservice
 Enterprise-Utilities

 currencyservice
 emailservice
 paymentservice
 Change Summary
 To make the changes listed above, we modified the release/kubernetes-manifest.yaml file to include namespaces for the deployments and modi

 Additional Notes
 There are several outstanding issue which still need to be addressed. Those include:

 SCC Context - to get the pods to run, we had to modify the default service account to use anyuid
 Persistent Storage - We would like to introduce historical purchase history data for the users purchases
 Authentication - We would like to identify the return users and provide them with the feature listed above
 Security Posture - We would like to lock the environment down to enforce tenant isolation, data segmentation, resource quotas and limits,
 Testing Procedure
 Still being designed. Will be listed on the page once we have finalized the v1 draft.

 Related PRs or Issues
N/A
---
