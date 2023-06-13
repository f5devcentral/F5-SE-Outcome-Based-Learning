Step 4 - Deploy the Site
========================

**Objective**:

Deploy the manifest for F5XC Kubernetes resources

**Why**:

The manifest contains all the resources needed to bring the F5XC site online

**How**:

From a command line with access to your Kubernetes environment type:

```kubectl apply -f <manifest>.yml```

**Validation**: 

Verify that F5XC site services are running with:

```kubectl get pods -n ves-system -o=wide```

Verify that a new site registration request has been generated:

```kubectl logs vp-manager-0 -n ves-system```