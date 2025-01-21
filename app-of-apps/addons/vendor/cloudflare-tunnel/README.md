# Cloudflare Tunnel

## Secrets

- <https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/deploy-tunnels/deployment-guides/kubernetes/#routing-with-cloudflare-tunnel>

```sh
kubectl create -n cloudflare secret generic tunnel-remote \
  --from-literal=token=$TUNNEL_TOKEN
```
