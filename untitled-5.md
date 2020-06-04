# Setup Local Kubernetes Cluster under 5mins with Minikube or Docker Desktop App for Mac

![](https://miro.medium.com/max/60/1*EpagOS9rnUAiFl88wpQEMw.jpeg?q=20)

Local Kubernetes Cluster

## Setup Local Kubernetes Cluster under 5mins with Minikube or Docker Desktop App for Mac

### What is Minikube? <a id="4e6b"></a>

[![Raymond](https://miro.medium.com/fit/c/96/96/0*sGGlLK_7Vq5zyYzK.jpeg)](https://medium.com/@aznric3boi91?source=post_page-----84bd5a8ab3d6----------------------)

Minikube is a tool that makes it easy to run Kubernetes locally. Minikube runs a single-node Kubernetes cluster inside a Virtual Machine \(VM\) on your laptop for users looking to try out Kubernetes or develop with it day-to-day.

### 1. Install Homebrew <a id="8c47"></a>

```text
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### 2. Install Minikube <a id="e46d"></a>

```text
$ brew tap caskroom/cask$ brew install kubernetes-cli
$ brew cask install minikube$ minikube --help
$ minikube --version
```

### 3. Install Kubectx <a id="1487"></a>

Kubectx aids us in writing more concise commands in the kubectl-cli. It aids us in changing context of where our kubernetes commands:

```text
// From This$ kubectl config use-context minikube// To This$ kubectx minikube
```

Learn more here: [https://kubectx.dev](https://kubectx.dev/)

```text
$ brew install kubectx
```

### 4. Start a minikube instance <a id="b0a9"></a>

```text
$ minikube start─ minikube start
😄  minikube v1.4.0 on Darwin 10.14.6
💿  Downloading VM boot image ...
    > minikube-v1.4.0.iso.sha256: 65 B / 65 B [--------------] 100.00% ? p/s 0s
    > minikube-v1.4.0.iso: 135.73 MiB / 135.73 MiB [-] 100.00% 8.27 MiB p/s 17s
🔥  Creating virtualbox VM (CPUs=2, Memory=2000MB, Disk=20000MB) ...
🐳  Preparing Kubernetes v1.16.0 on Docker 18.09.9 ...
💾  Downloading kubelet v1.16.0
💾  Downloading kubeadm v1.16.0
🚜  Pulling images ...
🚀  Launching Kubernetes ...
⌛  Waiting for: apiserver proxy etcd
 scheduler controller dns
🏄  Done! kubectl is now configured to use "minikube"
```

Alternatively you may download Docker.dmg and turn on kubernetes cluster within it’s system preferences.

![](https://miro.medium.com/proxy/1*OJ7itEpNdB6MRZRkAITlbw.png)

Once that is done. You can install the kubernetes dashboard via:

```text
$ kubectl create -f https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/recommended/kubernetes-dashboard.yaml$ kubectl get pods — namespace=kube-systemNAME                                       READY STATUS RESTARTS AGE...
kubernetes-dashboard-XXXXXXX-ctrtl      1/1   Running 0       3m$ kubectl port-forward kubernetes-dashboard-XXXXXXX-ctrtl 8443:8443 — namespace=kube-system
```

If you choose to use kubernetes with Docker Desktop App, you will have to create a deployment, spin up a service, and expose ports. To keep things simple we chose to use Minikube because it has everything built in.

### 5. Check Minikube Cluster status and dashboard <a id="7c3d"></a>

```text
$ minikube status╰─ minikube status
host: Running
kubelet: Running
apiserver: Running
kubectl: Correctly Configured: pointing to minikube-vm at 192.168.99.100$ minikube dashboard╰─ minikube dashboard
🔌  Enabling dashboard ...
🤔  Verifying dashboard health ...
🚀  Launching proxy ...
🤔  Verifying proxy health ...
🎉  Opening http://127.0.0.1:62337/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/ in your default browser...
```

![](https://miro.medium.com/proxy/1*EugMEml94hR07LsuIeDMQQ.png)

You should be able to take a look at the dashboard of the minikube cluster you have created in your browser.

### 6. Stopping Minikube cluster <a id="f5cc"></a>

```text
$ minikube stop╰─ minikube stop
✋  Stopping "minikube" in virtualbox ...
🛑  "minikube" stopped.
```

If you prefer to copy and paste installation and minikube cluster spinup:

```text
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"brew tap caskroom/cask
brew install kubernetes-cli
brew cask install minikubebrew install kubectxminikube start
minikube status
minikube dashboardminikube stop
```

Sum Up

* Install Kubernetes via homebrew or Docker.dmg
* Install kubectx to switch context easier in the future
* Serve up Kubernetes Dashboard and poke around to see what it looks like. Poke around the dashboard to what resources are being consumed.

The next post will talk about services and deployments! Stay tuned!

References:

\#kubernetes \#devops \#docker \#gcp \#eks \#tutorial \#minikube \#k8s \#easy \#cluster \#local \#mac

