# Deployment Instructions

```shell
oc apply -f ./.gitlab-ci-manifests/gitlab-runner-secret.yaml -n 360-consultant-feedback--default-team
oc apply -f ./.gitlab-ci-manifests/gitlab-runner.yaml -n 360-consultant-feedback--default-team
```
