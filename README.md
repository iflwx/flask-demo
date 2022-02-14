# flask-demo

## Step 0
Enable workflow for project.

## Step 1:
visit this repository, click ```Settings - Secrets - Actions - New repository secret```, and then add
- CI_TOKEN // ```Account - Settings - Developer Settings - Personal access tokens - Generate new token```
- USERNAME // docker hub username
- PASSWORD // docker hub password

## Step 2:
modify this repository to trigger CI actions.

It will trigger the action to build docker image and push it to docker hub, then update the docker image name and tag in ```kustomization.yaml``` in ```secret``` directory of project ```flask-demo-kustomize```, which can trigger afterwards Argo CD sync workflows.

You can check the process and result of the action by click ```Actions - Workflows - CI - build```

## Other
You can also manually trigger the action of project ```flask-demo-kustomize``` by click ```Actions - Workflows - CI - Run workflow``` and fill the docker image name and docker image tag fields.
