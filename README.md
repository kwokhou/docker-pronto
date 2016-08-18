## What is Pronto
Pronto is an automated code review tools created by Mindaugas @ https://github.com/mmozuras/pronto

## How to use this image

### Running Pronto

Inside a Ruby / Rails project directory, run:
```
docker run -v `pwd`:/data --rm kwokhou/pronto
```

 - `-v` maps your current directory to the `/data` directory insider the container.
 - `--rm` clean up the container after pronto finish running.

Running the image without and argument is equivalent of running `pronto run` (See `Dockerfile` of this repo). Similarly you can run: 
```
docker run -v `pwd`:/data --rm kwokhou/pronto pronto run
```

Check out https://github.com/mmozuras/pronto#usage for more details
