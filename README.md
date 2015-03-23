# ArchivaDocker
A docker image for Apache Archiva

The project is hosted on [Github](https://github.com/KamikazeLux/archivaDocker).

## Versions
Apache Archiva version 1.3.9

This docker image is tested with Docker 1.5.0

## Run
To run the image simply pull it and execute the following:

```Shell
docker run kamikazelux/archivadocker
```

## Container details
### Volume
If you want to persist the container data, you simple need to define a volume for `/var/archiva`.

```Shell
docker run -v /var/archiva kamikazelux/archivadocker
```

If you want to persist to a local folder use:

```Shell
docker run -v /path/to/local/folder:/var/archiva kamikazelux/archivadocker
```

### Ports
Apache Archiva is exposed through the port 8080. If you want to be able to access Apache Archiva via your browser you need to map the port to a port on your machine.

This command maps the local port 8080 to the container's port 8080:

```Shell
docker run -p 8080:8080 kamikazelux/archivadocker
```


### All together

```Shell
docker run -d -p 8080:8080 -v /local/folder:/var/archiva --name="archiva" kamikazelux/archivadocker
```

## Issues & Improvements
For issues and improvements contact us on [Github](14318410005).
