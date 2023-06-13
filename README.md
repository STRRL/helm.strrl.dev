# STRRL Personal Helm Repository

Add strrl.dev repository to Helm repos:

```bash
helm repo add strrl.dev https://helm.strrl.dev
```

Search available version:

```bash
helm search repo strrl.dev
```

## Install Cloudflare Tunnel Ingress Controller

```bash
helm upgrade --install --wait \
  -n cloudflare-tunnel-ingress-controller --create-namespace \
  cloudflare-tunnel-ingress-controller \
  strrl.dev/cloudflare-tunnel-ingress-controller \
  --set=cloudflare.apiToken="<cloudflare-api-token>",cloudflare.accountId="<cloudflare-account-id>",cloudflare.tunnelName="<your-favorite-tunnel-name>" 
```
