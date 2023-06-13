Step 3 - Create a Manifest File
=============================

**Objective**:

Create a manifest file containing Kubernetes resources for the F5XC site

**Why**:

There are two methods of deploying an F5XC site into a container environment, Kubernetes manifests, and Helm. Manifests are the quickest path without needing to install Helm. However, in more automated deployments Helm would be preferred as it can be templated for reuse in different environments.

Read about Helm: https://helm.sh/

**How**:

Download the F5XC kubernetes manifest: https://gitlab.com/volterra.io/volterra-ce/-/blob/master/k8s/ce_k8s.yml

After downloading the manifest it will need to be edited. Under the configmap resource section user input is needed, look for the below and modify it for your location/name:

```
data: 
 config.yaml: | 
  Vpm:
    # CHANGE ME
    ClusterName: <cluster name>
    ClusterType: ce
    Config: /etc/vpm/config.yaml
    DisableModules: ["recruiter"]
    # CHANGE ME
    Latitude: <latitude>
    # CHANGE ME
    Longitude: <longitude>
    MauriceEndpoint: https://register.ves.volterra.io
    MauricePrivateEndpoint: https://register-tls.ves.volterra.io
    PrivateNIC: eth0
    SkipStages: ["osSetup", "etcd", "kubelet", "master", "voucher", "workload", "controlWorkload"]
    # CHANGE ME
    Token: <token>
    CertifiedHardware: k8s-minikube-voltmesh
```

Latitude and Longitude are used as geo markers for the F5XC site, the two closest F5XC regional edges will become peers. Choose a lat/long location closest to your physical environment.

**Validation**: 

The manifest file has been modified and saved.