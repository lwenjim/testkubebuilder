# testkubebuilder
## see: https://book.kubebuilder.io/cronjob-tutorial/running
## see:https://lailin.xyz/post/operator-04-kustomize-tutorial.html
```bash
kubebuilder init --domain tutorial.kubebuilder.io --repo tutorial.kubebuilder.io/project
kubebuilder create api --group batch --version v1 --kind CronJob
kubebuilder create webhook --group batch --version v1 --kind CronJob --defaulting --programmatic-validation
export ENABLE_WEBHOOKS=false
kubectl get cronjob.batch.tutorial.kubebuilder.io -o yaml
kubectl get job
```