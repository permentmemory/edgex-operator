# Using k8s operator to deploy EdegxFoundry   
## Prerequisites 
- operator-sdk v1.0.0  
- Kubernetes v1.16.0+ cluster  
- helm chart  
## Installation    
- deploy crd  
	<pre>
     cd edgex-operator
     kubectl apply -f /config/crd/base/edgex.deploy_edgices.yaml
    </pre>  
- run operator-sdk outside the cluster  
	<pre>
     make run
    </pre>  
- deploy edgex cr  
    <pre>
      kubectl apply -f config/samples/edgex_v1_edgex.yaml
    </pre>  
## Uninstallation  
- uninstall
    <pre>
     kubectl delete Edgex edgex-sample
     kubectl delete crd edgexs.edgex.deploy
    </pre>  
## Relevant reference  
Running operator-sdk as a pod inside a Kubernetes cluster  
[reference](https://sdk.operatorframework.io/docs/building-operators/helm/tutorial/)
    
    
