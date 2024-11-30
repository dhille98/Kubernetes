# pod scurity scan 

* using the kubesec-scan
* installations documents 
* [Refer here](https://github.com/controlplaneio/kubesec/releases) installation offical docs
* after install `tar -xvzf ` and `mv kubesec /usr/local/bin` and `chmod 777 kubesec`
*  scan the yaml file `kubesec scan pod.yaml`
*  
### Best Practices for Improving Your Score
* To improve your Kubesec score and enhance the security of your Kubernetes deployments, consider implementing the following practices:
* **Avoid Privileged Containers:** Ensure that containers do not run in privileged mode unless absolutely necessary.
* **Use Non-Root Users:** Configure containers to run as non-root users by setting runAsUser and runAsNonRoot in the security context.
* **Set Resource Limits:** Define CPU and memory limits to prevent resource exhaustion attacks.
* **Implement Security Contexts:** Use Kubernetes security contexts to restrict capabilities and enforce read-only filesystems.
* **Utilize Service Accounts:** Assign service accounts with the least privilege necessary for your applications.
* **Apply Network Policies:** Control traffic flow between pods to minimize exposure to potential attacks.