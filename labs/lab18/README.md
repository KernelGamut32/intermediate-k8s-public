# Lab 18 - Ingress

Walk through the tutorial defined at https://matthewpalmer.net/kubernetes-app-developer/articles/kubernetes-ingress-guide-nginx-example.html. Utilize either a local instance of k8s using Docker-Desktop with Kubernetes enabled (or another comparable option) or a remote instance to which you have permission to execute resource creation against.

Use the files available in the solution folder (the files in the tutorial need adjustments) as a guide along with these additional instructions:

* Execute `kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.8.2/deploy/static/provider/cloud/deploy.yaml` to pull down the nginx ingress controller to your cluster
* This will create a new namespace called `ingress-nginx` - use `kubectl get pods -n ingress-nginx` to see the pods created with the ingress controller
* From the solution folder (or your own folder if you are self-coding), apply the appropriate Kubernetes manifests for the resources you wish to deploy
* You can use `curl http://localhost/apple` and `curl http://localhost/banana` to verify