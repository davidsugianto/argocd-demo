# argocd-demo
GitOps Implementation on sample web application using Argo CD

automatically syncronize with plugin kustomize.io:

- Create kutomization.yaml in applications/staging and applications/production

  kustomization.yaml in staging:
  ```
  apiVersion: kustomize.config.k8s.io/v1beta1
  kind: Kustomization
  resources:
  - deployment.yaml
  namespace: staging-app
  images:
  - name: idiots718/nuxtjs-basic-ssr
    newTag: 0.3
  ```

  kustomization.yaml in prodcution:
  ```
  apiVersion: kustomize.config.k8s.io/v1beta1
  kind: Kustomization
  resources:
  - deployment.yaml
  namespace: production-app
  images:
  - name: idiots718/nuxtjs-basic-ssr
    newTag: 0.3
  ```


