# Docker hub demo

### Configuring credentials.

First you need to update the Maven [settings.xml](https://dmp.fabric8.io/#authentication) with your Docker Hub's credentials.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<servers>
    <server>
        <id>docker.io</id>
        <username>jolokia</username>
        <password>s!cr!t</password>
    </server>
    ....
</servers>
```

Also is necessary update where the image will be pushed

```xml
<verbose>true</verbose>
<registry>registry.hub.docker.com/yourusername</registry>
<images>
```



### Generate image and push to docker registry.

```
mvnn clean install
```
