# dockerfiles
Various Docker Files

## heavy-jupyter
Container for [jupyter](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html) notebooks with :
 - [gpu support](https://github.com/iot-salzburg/gpu-jupyter)
 - C++ kernel support with [xeus-cling](https://github.com/jupyter-xeus/xeus-cling)

To build and use from this repo:
```bash
docker-compose -f "heavy-jupyter/docker-compose.yml" up -d --build
```

To use prebuilt image:
```
docker pull bricegros/heavy-jupyter
docker run -d -P --net=host -v ./data:/home/jovyan/work bricegros/heavy-jupyter
```

Then, open a browser to localhost:8888, use `asdf` when prompted
