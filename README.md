# Image construction

```bash
cd build
docker build . -t php_backend_dev
```

# Image launch
Go to the parent directory
```bash
cd ..
docker run -d --rm -p 8080:80 -p 8000:8000 --name backend -v %CD%/volume:/volume --ip 192.168.33.225 php_backend_dev
```
**docker run** to create virtualization of the image.

**-d** For stdout output.

**--rm** delete the container when the virtualization is finished.

**-p** real port corresponds to the virtual port. realport:virtuelport

**--name** Name of virtualization to start or stop.

**-v** Real folder corresponds to the virtual folder.

**php_backend_dev** Name of our image to running.

# Source code for work
In the folder / volume / backend / public

## Access to bash
```bash
docker exec -it backend bash
```

## URLs access
look at the correct ip with ipconfig command

**PHP server adress** [http://192.168.33.225:8000/](http://192.168.33.225:8000/)

**phpmyadmin server adress** [http://192.168.33.225:8080/](http://192.168.33.225:8080/)