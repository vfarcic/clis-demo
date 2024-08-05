# Demo Manifests and Code Used in DevOps Toolkit Videos

[![Why I Can't Live Without These 10 CLIs!](https://img.youtube.com/vi/7ItANF7eytU/0.jpg)](https://youtu.be/7ItANF7eytU)l cnpg cloudnative-pg \
    --repo https://cloudnative-pg.github.io/charts \
    --namespace cnpg-system --create-namespace --wait

helm upgrade --install atlas-operator \
    oci://ghcr.io/ariga/charts/atlas-operator \
    --namespace atlas-operator --create-namespace --wait

timoni build silly-demo timoni \
    --values timoni/values-db-cnpg.yaml --namespace a-team \
    | kubectl apply --filename -
```

## App with OTEL

```sh
kubectl create namespace a-team

timoni build silly-demo timoni \
    --values timoni/values-otel.yaml --namespace a-team \
    | kubectl apply --filename -
```
