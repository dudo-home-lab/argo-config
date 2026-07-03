# OpenTelemetry Demo Application

To set up the database connection strings for the demo applications, you can create a Kubernetes secret with the necessary DSN values. Use the following command to create the secret in the `opentelemetry-demo` namespace:

```sh
kubectl create secret generic otel-demo-db -n opentelemetry-demo \
  --from-literal=accounting-dsn='Host=otel-demo-rw.cnpg-system.svc.cluster.local;Username=user;Password=password;Database=otel' \
  --from-literal=reviews-dsn='host=otel-demo-rw.cnpg-system.svc.cluster.local user=user password=password dbname=otel sslmode=disable' \
  --from-literal=catalog-dsn='postgres://user:password@otel-demo-ro.cnpg-system.svc.cluster.local/otel?sslmode=disable'
```
