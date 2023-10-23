## Compliance Operator Chart

### Installation

```bash
### Add and Update the Helm Repository
helm repo add ocac-charts https://opencomplianceascode.github.io/charts
helm repo update

### Create the Compliance Operator Namespace
kubectl create namespace openshift-compliance

### Fetch the Compliance Operator Values File
curl -#OL https://raw.githubusercontent.com/OpenComplianceAsCode/charts/main/charts/compliance-operator/rke2-values.yaml

### Install the Compliance Operator
helm upgrade -i compliance-operator ocac-charts/compliance-operator-chart --namespace openshift-compliance -f rke2-values.yaml
```