
# Kubernetes Commands with Explanation

## 1. **Setting Up Docker**

- **`sudo apt-get update`**
  - *Description*: Updates the package list to ensure the latest versions are available.
  - *Meaning*: Prepares your system for installing the latest software.

- **`sudo apt-get install docker.io -y`**
  - *Description*: Installs Docker on your system.
  - *Meaning*: Ensures Docker is ready for container management.

- **`sudo usermod -aG docker $USER`**
  - *Description*: Adds your user to the `docker` group.
  - *Meaning*: Allows running Docker commands without using `sudo`.

- **`sudo newgrp docker`**
  - *Description*: Refreshes your group membership for Docker without needing to log out.
  - *Meaning*: Makes the `docker` group changes effective immediately.

---

## 2. **Docker Commands**
- **`docker ps`**
  - *Description*: Displays a list of running Docker containers.
  - *Meaning*: Helps you check the status and details of your containers.

- **`clear`**
  - *Description*: Clears the terminal screen.
  - *Meaning*: Useful for making the terminal clutter-free.

---

## 3. **Installing Kind (Kubernetes in Docker)**
- **`[ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.25.0/kind-linux-amd64`**
  - *Description*: Downloads the Kind binary for AMD64 architecture.
  - *Meaning*: Ensures you're downloading the right version for your system.

- **`chmod +x ./kind`**
  - *Description*: Makes the downloaded Kind binary executable.
  - *Meaning*: Prepares the binary for running commands.

- **`sudo mv ./kind /usr/local/bin/kind`**
  - *Description*: Moves the Kind binary to a directory in your PATH.
  - *Meaning*: Allows you to use the `kind` command from anywhere.

- **`kind`**
  - *Description*: Verifies that Kind is installed successfully.
  - *Meaning*: Running `kind` confirms the installation.

---

## 4. **Validating and Installing kubectl**
- **`echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check`**
  - *Description*: Validates the downloaded kubectl binary's checksum.
  - *Meaning*: Ensures the file's integrity before installation.

- **`sudo snap install kubectl`**
  - *Description*: Installs kubectl using Snap.
  - *Meaning*: Quickly gets kubectl ready to use.

- **`sudo snap install kubectl --classic`**
  - *Description*: Installs kubectl in classic mode.
  - *Meaning*: Provides extended permissions for traditional Linux systems.

- **`kubectl version`**
  - *Description*: Displays the installed kubectl version.
  - *Meaning*: Confirms installation and compatibility.

---

## 5. **Cluster Management with Kind**
- **`kind create cluster --name=my-cluster`**
  - *Description*: Creates a Kubernetes cluster named `my-cluster` using Kind.
  - *Meaning*: Sets up a local Kubernetes environment.

- **`kind get cluster`**
  - *Description*: Lists the Kind clusters created.
  - *Meaning*: Verifies cluster creation.

- **`kubectl get nodes`**
  - *Description*: Retrieves information about cluster nodes.
  - *Meaning*: Confirms the cluster's node readiness.

- **`kind delete cluster --name=my-cluster`**
  - *Description*: Deletes the cluster named `my-cluster`.
  - *Meaning*: Cleans up the environment.

---

## 6. **Namespace Management**
- **`kubectl get ns`**
  - *Description*: Lists all namespaces in the cluster.
  - *Meaning*: Helps identify namespace availability.

- **`kubectl create ns dev`**
  - *Description*: Creates a namespace called `dev`.
  - *Meaning*: Provides a separate space for development workloads.

- **`kubectl delete ns dev`**
  - *Description*: Deletes the `dev` namespace.
  - *Meaning*: Removes the development namespace when it's no longer needed.

---

## 7. **Deploying and Inspecting Pods**
- **`kubectl run nginx --image=nginx`**
  - *Description*: Creates a pod named `nginx` using the `nginx` image.
  - *Meaning*: Quickly deploys a simple web server pod.

- **`kubectl get pods`**
  - *Description*: Displays all pods running in the current namespace.
  - *Meaning*: Helps track pod status.

- **`kubectl describe pod/nginx`**
  - *Description*: Shows detailed information about the `nginx` pod.
  - *Meaning*: Useful for debugging and monitoring pod activities.

---

## 8. **Cluster Deletion**
- **`kind delete cluster --name=my-cluster`**
  - *Description*: Deletes the specified Kind cluster.
  - *Meaning*: Removes the cluster to free resources.

- **`clear`**
  - *Description*: Clears the terminal for a fresh start.
  - *Meaning*: Maintains a clean workspace.

---

## 9. **File and Directory Operations**
- **`mkdir k8s-practise`**
  - *Description*: Creates a directory named `k8s-practise`.
  - *Meaning*: Prepares a workspace for Kubernetes practice.

- **`cd k8s-practise/`**
  - *Description*: Changes the directory to `k8s-practise`.
  - *Meaning*: Navigates into the practice workspace.

- **`vim config.yml`**
  - *Description*: Opens a new configuration file in the Vim editor.
  - *Meaning*: Starts editing the cluster configuration file.

---
