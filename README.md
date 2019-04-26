# What
Template for python app connecting to spark cluster running in Docker containers.

## Background
Made to use using https://github.com/big-data-europe/docker-spark

## Launch
To build and run the image. Make sure to par special attention to the network name, as it is set automatically by bde2020/docker-spark.
To run the container in the background, please add the -d flag.

```
docker build --rm -t connect-to-spark .
docker run --rm --name my-spark-app -e ENABLE_INIT_DAEMON=false --link spark-master:spark-master --net docker-spark_default connect-to-spark
```
