  1 ## Worklog
  2
  3 The Microservices Demo provided by Google is a good starting base for a multifunction SaaS.
  4
  5 The comments from the last pull request in it's previous repo loaction is listed below for documentation:
  6
  7 ---
  8 PR: Service split 1
  9
 10 Background
 11 The base repository was written by Google and was designed to have all of the services within one namespace. Additionally, while the proje
 12 Due to the enhanced security in OpenShift, and the want to segment roles and responsibilities for the microservices, we forked the origina
 13
 14 Fixes
 15 Segmented the microservices into the following namespaces:
 16
 17 Client1:
 18
 19 adservice
 20 rediscart
 21 frontend
 22 Boutique-Ops
 23
 24 cartservice
 25 checkoutservice
 26 loadgenerator
 27 productcatalog
 28 recommendationservice
 29 shippingservice
 30 Enterprise-Utilities
 31
 32 currencyservice
 33 emailservice
 34 paymentservice
 35 Change Summary
 36 To make the changes listed above, we modified the release/kubernetes-manifest.yaml file to include namespaces for the deployments and modi
 37
 38 Additional Notes
 39 There are several outstanding issue which still need to be addressed. Those include:
 40
 41 SCC Context - to get the pods to run, we had to modify the default service account to use anyuid
 42 Persistent Storage - We would like to introduce historical purchase history data for the users purchases
 43 Authentication - We would like to identify the return users and provide them with the feature listed above
 44 Security Posture - We would like to lock the environment down to enforce tenant isolation, data segmentation, resource quotas and limits,
 45 Testing Procedure
 46 Still being designed. Will be listed on the page once we have finalized the v1 draft.
 47
 48 Related PRs or Issues
 49 N/A
 50 ---
 51
 52
