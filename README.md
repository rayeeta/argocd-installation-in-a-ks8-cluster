#### Commands

```bash
# install ArgoCD in k8s
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# access ArgoCD UI
kubectl get svc -n argocd
kubectl port-forward svc/argocd-server 8080:443 -n argocd

# login with admin user and below token (as in documentation):
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo

# you can change and delete init password

```
</br>

#### Links

* Config repo: (https://github.com/rayeeta/argocd-project/tree/master)
  
* Docker repo: [https://hub.docker.com/repository/docker/ereta19/argocdproject/general](https://hub.docker.com/repository/docker/ereta19/argocdproject/general)

* Install ArgoCD: [https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)

* Login to ArgoCD: [https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli](https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli)

* ArgoCD Configuration: [https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/](https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/)


# What is Gitops?
GitOps is an operational framework that applies DevOps principles, such as version control and continuous integration/continuous delivery (CI/CD), to the management of infrastructure. It automates the provisioning and configuration of infrastructure by using Git repositories as the central source of truth for defining the desired state of systems.
In GitOps, teams utilize configuration files stored in Git, allowing them to manage infrastructure in a manner similar to how they handle application code. This approach enhances visibility and traceability of changes, making it easier to audit and reproduce issues. By leveraging familiar Git workflows, GitOps empowers developers to take on operational tasks, streamlining the deployment process and improving agility in responding to changes.
GitOps is particularly effective in cloud-native environments, such as those using Kubernetes, where it facilitates continuous deployment and infrastructure management through declarative specifications. Overall, GitOps represents an evolution of Infrastructure as Code (IaC), enabling teams to automate and manage their infrastructure efficiently while maintaining a clear audit trail of all changes.




