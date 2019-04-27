# K8S-DASHBOARD
You need to set up the k8s-dashnoard only.

Kubernetes Dashboard is a general purpose, web-based UI for Kubernetes clusters. It allows users to manage applications running in the cluster and troubleshoot them, as well as manage the cluster itself.

Dashboard UI workloads page

Getting Started
IMPORTANT: Read the Access Control guide before performing any further steps. The default Dashboard deployment contains a minimal set of RBAC privileges needed to run.

To deploy Dashboard, execute following command:

$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v1.10.1/src/deploy/recommended/kubernetes-dashboard.yaml
To access Dashboard from your local workstation you must create a secure channel to your Kubernetes cluster. Run the following command:

$ kubectl proxy
Now access Dashboard at:

http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/.

Create An Authentication Token (RBAC)
To find out how to create sample user and log in follow Creating sample user guide.

NOTE:

Kubeconfig Authentication method does not support external identity providers or certificate-based authentication.
Dashboard can only be accessed over HTTPS
Heapster has to be running in the cluster for the metrics and graphs to be available. Read more about it in Integrations guide.
Documentation
Dashboard documentation can be found on Wiki pages which contains:

Common: Entry-level overview
User Guide: Installation, Accessing Dashboard and more for users
Developer Guide: Getting Started, Dependency Management and more for anyone interested in contributing
Community, discussion, contribution, and support
Learn how to engage with the Kubernetes community on the community page.

You can reach the maintainers of this project at:

#sig-ui on Kubernetes Slack
kubernetes-sig-ui mailing list
Issue tracker
SIG info
