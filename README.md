Set local gcloud to new project
```
gcloud auth application-default set-quota-project sep-poc-aa-hackathon-prj
gcloud config set project sep-poc-aa-hackathon-prj
```

To get GKE cluster credentials
```
gcloud container clusters get-credentials primary --zone us-central1-a --project sep-poc-aa-hackathon-prj
```

Gcloud Auth login
```
gcloud auth login
```

To use in Lens & run k8s commands
```
gcloud components install gke-gcloud-auth-plugin
also require in ~/.zshrc 
export USE_GKE_GCLOUD_AUTH_PLUGIN=False
```

To configure in  local
```
 gcloud auth configure-docker us-central1-docker.pkg.dev
```

To list of available images
```
gcloud artifacts docker images list us-central1-docker.pkg.dev/sep-poc-aa-hackathon-prj/aa-gcr
```

To describe a repository
```
 gcloud artifacts repositories describe aa-gcr --project=sep-poc-aa-hackathon-prj --location=us-central1
```


To view Ingress IP
```
 k get svc -n ingress
```

To apply changes
```
k apply -f example.yaml
k apply -f service.yaml
```