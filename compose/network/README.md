

## ACME for Traefik

```
https://doc.traefik.io/traefik/reference/install-configuration/tls/certificate-resolvers/acme/#wildcard-domains

https://jaredheinrichs.substack.com/p/how-to-setup-cloudflare-letsencrypt
```

## AdguardHome quic

For AdguardHome to properly query upstream DNS servers through quic protocol ensure the host has below

```
echo "net.core.rmem_max = 7500000
net.core.wmem_max = 7500000" | sudo tee /etc/sysctl.d/99-net-buffers.conf

cat /etc/sysctl.d/99-net-buffers.conf

sudo sysctl --system

```

Reference: 'https://github.com/quic-go/quic-go/wiki/UDP-Buffer-Sizes'
