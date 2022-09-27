### Deploying WordPress using kubernetes manifests

Prerequisites: install docker and k8s

1. Creating a mysql deployment to a replica and exposing the pods with the ClusterIP service
	- Apply : `kubectl apply -f mysql-wordpress.yml`
    - Verify : `kubectl get all -o wide`
                   `kubectl describe svc name_service`
                   
2. Creation of a wordpress deployment with the right variables to connect to the mysql database.
The deployment stores the wordpress data on a volume mounted in the /data of the node.
The wordpress frontend is exposed with the NodePort service.

	- Apply: `kubectl apply -f wordpress.yml`

	- Verify: `kubectl get all -o wide`
                   `kubectl describe svc name_service`

![](https://lh5.googleusercontent.com/M6t7D-EnA43limKCYN-uoUezclJZ1qFpHiaYK6hufkEGhAI1mRHXv6v57ZMTov0HYPOMtHztX9mD1jdmXnyRhE7NLi9LbEp19UuwIY7k9Sr179T8UkkIebjfyC416nMcb1J5Y6G81su7kKbC0L9DF8Dh1DP86Gr7l9TYIxRAywgV0xrBwXFqPyexPg)

![](https://lh5.googleusercontent.com/Zmpr9FHjharPuxI3ijOc2GVEHagN1MnP7GqqwjQBmY4gzvyDD8LOsKgrPTMZstOD4iBZgTeVOfghLh6h6jxcOYOKkNOgI3xutr0jxjOg1AT9mItw5JumnjJfvlAUZWchNWucFBaYY1nfhUMLvZSOe3ttjigRFTKJV_9nD3Mj00UXNN8KFDmzap9GNw)

![](https://lh4.googleusercontent.com/IdtuSE7keVLLeaOEGiM9z97zQugLMGX7LplSD03Q5zuWrh1HjxjtkK2-e4iC_tNGwhW1HUvEAvkmwfxjYBEZHyifCsmSWY5a83jiBMDYKsBN4pfXjhR5rWJNyhLkYAQjkQUNK_E2rhSvyW8Jyd6Yf1XVUaBQnKpovDy40bDZKSELiTd9Yv9cSysIOw)

![](https://lh4.googleusercontent.com/iT0jV57dLi9aykwjfyR1vpAAz_0M4UBebJFesTJUNN6GBlQgd5sP_-o0M_LSjzpmwWP575LqsXIrEslOlTWPV_FRdiOmaPuUIgQt7UbB1cG-aBKY7RFbAnCOjdAxHXd9zImx-ZvnuNsmN5oQP8nU2fMSPQxRxf_CQA7WFMlSbbDpFsyCQ4SKIRrqag)# WordPress-Kubernetes
