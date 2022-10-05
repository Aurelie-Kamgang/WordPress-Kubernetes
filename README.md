
### Deploying WordPress using kubernetes manifests

Prerequisites: install docker and k8s

1. Creating a mysql deployment to a replica and exposing the pods with the ClusterIP service
                   
2. Creation of a wordpress deployment with the right variables to connect to the mysql database.
The deployment stores the wordpress data on a volume mounted in the /data of the node.
The wordpress frontend is exposed with the NodePort service.
- create data host path: `mkdir /data && mkdir /data/mysql && mkdir /data/wordpress`
 - apply: `kubectl apply -k .`
 - verify: `kubectl get all -o wide -n wordpress`
 
 **![](https://lh4.googleusercontent.com/AyB5gIdgvKsQv4An3s0rw16A4zSQNp2u-Y5allMZn5aYWOCGwpVNHk9IDx4F36uztcURtDvQ_RJfdXBdVvuuu6khRMPZiGqBgScAumg-1LWLHY9BLS-SqXNY1-3GtySWOAgw6QBVGTs_NEkXjOFDkTi9QU4fXdXP1WKTud8ZSxEgaWXbLPtbcGkUUA)**
 **![](https://lh4.googleusercontent.com/t2tJXNAiJrvUqb_sMrBLhqDPSGBo7HJMX-NNcBXjp52Qg4j_VLVzRv-OjI_k183GS3YAuyVZWZ-C7iCpZwKrvXM5AZ2MC37lfeGYUW8Ibb-o4jL4KZn6apDWPFrN-Z4Z-u6KBq3GTJ9GGkz7_pZLPnhxO8Qi6hsPsy2rwBiWCiiKz-UE0wqgl3jIoQ)**
 **![](https://lh3.googleusercontent.com/QkHF0M60W7mUlfmrz2dfoAAOcvEP7KPlKZXDLhKLFEXOuve3RSFlnrSCBQ6Kl6dtjdOrED6FaYorCOOfTBgmGsSdsXlKEy_l1wUSPbJH-IiAodmK-t-_qae1Xud7zFBabwz4C438Xm6Q28Atb4XL3i3Yvf9HxQqDHpmM8YiHBByT8k_KogMBx_L3RA)**
 **![](https://lh5.googleusercontent.com/Gr-HUSz0PO4rTuGXwu3hURGsWcWbnioBJSkHysRL1lFqwQ-ZGnOV8q8WJLhowPnxxh86gsrAPUMnf02wvCSvieXvWQFELjeq7-DtQfvdx5cFkp-hJuipwgayyOyVs_cSnFXimsCaiCsHhRZ8qQAeMxrF1iKuAEaeb_-7JKxUmcwu9iPdC93-rgtOiw)**
