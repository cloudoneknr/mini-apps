docker build  -t hell-app .
docker run -p 5000:5000 hello-app #for testing locally

docker build  -t ghcr.io/cloudoneknr/hello-app:latest .
docker login ghcr.io -u cloudoneknr
docker push ghcr.io/cloudoneknr/hello-app:latest

kubectl create secret docker-registry hello-minikube  --docker-server=https://ghcr.io --docker-username=XXXXXXXXX --docker-password=ghp_XXXXXXXXXXXXXXXXXX --docker-email=XXXXXXXXXX@gmail.com --dry-run=client -o yaml
