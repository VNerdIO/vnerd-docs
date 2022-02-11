# Home

Here are some docs...

Start with a working dockerfile and a docker installation. Test it locally

```
git clone https://github.com/VNerdIO/docs-container
cd docs-container

docker build -t vnerddocs .
sudo docker run -d -p 80:80 vnerddocs
```

Make sure you can connect to http://localhost. Tweak ports in `default.conf` and `dockerfile` if port 80 is in use.

Create an Azure Container registry and push your image. Your url below will be different.

```
sudo docker tag vnerddocs vnerdacr.azurecr.io/vnerddocs
sudo docker push vnerdacr.azurecr.io/vnerddocs
```

Create a containre instance in Azure from ACR and your repo above.