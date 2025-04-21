# jenkins-k8s-ansible
# Jenkins on Kubernetes via Ansible

This project deploys Jenkins to a Kubernetes cluster using Ansible and the `kubernetes.core` collection.

## 🧰 Prerequisites

- `ansible` installed
- `kubectl` configured to access your cluster
- `kubernetes.core` collection:
  ```bash
  ansible-galaxy collection install kubernetes.core

 # Deploy
 ansible-playbook playbook.yml

# Access jenkins
Visit http://<Node-IP>:30080 in your browser
kubectl exec -it jenkins -- cat /var/jenkins_home/secrets/initialAdminPassword
