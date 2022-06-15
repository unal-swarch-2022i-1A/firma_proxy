# firma_proxy

## Docker
Compílamos la imagen
```bash
docker build -t "firma_proxy" .
```

Lanzamos el contenedor y asignamos el dominio `host.docker.internal` a la ip del host
```bash
docker run -dit --name firma_proxy \
    --add-host=host.docker.internal:host-gateway \
    -p 80:80 \
    firma_proxy
```

Revisamos los logs
```bash
docker logs --tail 1000 -f firma_proxy
```