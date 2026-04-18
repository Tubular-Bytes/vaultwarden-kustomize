# vaultwarden-kustomize

Minimalist VaultWarden deployment using Kustomize.

[VaultWarden Wiki](https://github.com/dani-garcia/vaultwarden/wiki)  
[Kustomize Documentation](https://k8s.info/docs/core/kustomize)

```
# The env file contains the configuration. It will be mounted as environment variables via a secret
$ cp properties/.env.sample properties/.env

# The ingress patch is for defining the hostname for the ingress without having to commit it to git.
$ cp patches/ingress-patch.json.sample patches/ingress-patch.json

$ kubectl apply -k .