# Openshift commands
- oc login command -u → To Login to OpenShift
(Once Logged in, will have to create a new Project to start our work)
- oc cluster-info → To view Cluster info
- oc get --raw /healthz → To get Cluster status
- oc get all → Gives us a summary of the Resources for the current project you're using in OpenShift.
- oc projects → To list all projects
- oc new-project PROJECT_NAME → To create new Project
- oc project PROJECT_NAME → To change to a particular Project 
- oc new-app <container image> → Deploying an Application
- oc api-resources → Helps us understand which Resources need Namespace
- oc expose svc/<service name> → Expose an Application via Route
- oc create role <role name> --verb=<verbs> --resource=<resources> --namespace=<namespace>
- oc policy add-role-to-user <role name> -z <service account> -n <namespace>
→ Create a Role and Bind to a User or Service Account
- oc create route edge <route name> --service=<service name> → Create a Route
- oc expose svc/<service name> --port=<port> → Expose Ports in a Service
- oc adm taint node <node name> <taint key>=<taint value>:<taint effect> → Apply taint to a Node
- oc adm upgrade → To upgrade a cluster
- oc get nodes → Gets status of Nodes
- oc get pods → Gets status of all Pods
- oc get co → Prints out all the Cluster Operators
- oc describe pod/POD_NAME → To get more info about the Pod
- oc describe node/NODENAME → To get more info about the Node
- oc –-help → To get more information about all the commands present
- oc COMMAND --help → To get info about a specific command
