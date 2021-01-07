*Weave Scope is a visualization and monitoring tool for Docker and Kubernetes. It provides a top down view into your app as well as your entire infrastructure, and allows you to diagnose any problems with your distributed containerized app, in real time, as it is being deployed to a cloud provider.*


# Follow this link for the installation :

> https://www.weave.works/docs/scope/latest/installing/#k8s

# Open Scope in Your Browser

> kubectl port-forward -n weave "$(kubectl get -n weave pod --selector=weave-scope-component=app -o jsonpath='{.items..metadata.name}'')" 4040
                                  
                                   OR

> kubectl edit svc <service_name> -n <namespace>
and change service type to loadbalnacer or nodeport
