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

### Running Pronto on Bitbucket

To run Pronto against a Bitbucket repo, you can run the following command:
```
docker run -v `pwd`:/data --rm -e "BITBUCKET_USERNAME=MYUSERNAME" -e "BITBUCKET_PASSWORD=MYPASSWORD" kwokhou/pronto pronto run -f bitbucket -c origin/development
```

 - `-f` is the output formatters
 - `-c` is the commit to run `diff`. (Here it `diff` against the `development` branch)

Check out https://github.com/mmozuras/pronto#usage for more details
