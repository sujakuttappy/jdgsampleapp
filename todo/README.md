# datagrid-xpaas-demo-app

Forked from original example to make a couple of small usability "tweaks".

Deployment instructions -
* Tested with S2I jboss-eap64-openshift:1.2 Image
* Dependent on datagrid65-basic:1.2 Image, deployed separately in target OpenShift Project
* Requires additional Environment Variable in Deployment Configuration - JDG_SERVICE_NAME=DATAGRID_APP (assumes default naming conventions for Data Grid Deployment used)
* Update the default services account, to enable access to the kubernetes API - "oc policy add-role-to-user view system:serviceaccount:$(oc project -q):default -n $(oc project -q)"
