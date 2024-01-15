### Docker compose watch && Skaffold && Tilt usage example

#### Docker compose watch
```bash
docker compose watch
```

#### Skaffold
```bash
skaffold dev -f deploy/skaffold.yaml --port-forward=pods
```

#### Tilt
```bash
tilt up -f deploy/Tiltfile
```