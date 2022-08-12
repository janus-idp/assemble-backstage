# Deployment Instructions

```shell
#oc adm policy add-scc-to-user anyuid -z gitlab-runner-sa -n 360-consultant-feedback--default-team
#oc delete configmap ocp-config-toml -n 360-consultant-feedback--default-team
oc create configmap ocp-config-toml --from-file config.toml=./.gitlab-ci-manifests/config.toml -n 360-consultant-feedback--default-team
oc apply -f ./.gitlab-ci-manifests/gitlab-runner-secret.yaml -n 360-consultant-feedback--default-team
oc apply -f ./.gitlab-ci-manifests/gitlab-runner.yaml -n 360-consultant-feedback--default-team
```
