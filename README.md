# Charts
Helm charts for k8s homelabbing

## Tandoor

The `recipes` chart implements Tandoor v2.3.6; this chart requires a secret for login credentials to Tandoor and the supporting Postgres database.

To quickly create the required secret, run the following:

```bash
k -n tandoor create secret generic recipes-login --from-literal=username=ezferdm --from-literal=password=$(openssl rand -hex 64) --from-literal=secret-key=$(openssl rand -hex 64)
```

This should be automatically created in a future version of the chart.
