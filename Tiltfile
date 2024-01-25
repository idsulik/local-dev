k8s_yaml('./deploy/kubernetes.yaml')
docker_build(
    'skaffold-buildpacks-node', 
    context='.', 
    dockerfile='deploy/Dockerfile',
    live_update=[
        sync('./web', '/app'),
        run(
            'cd /app && npm install', 
            trigger=['./web/package.json']
        )
    ]
)
k8s_resource('web', port_forwards=3000)