# asap-infovyz

ASAP examples using infovyz library.

Please keep in mind the goal of these demos is to demonstrate general library functionality. The ElasticSearch instance is not optimized towards production ready security and performance.

## Configuration

After checking out this repository, run `npm install` to load required dependencies. To run the example, you'll need `docker` and `docker-compose` to work on your local machine. If you run docker inside a local virtual machine, you'll have to change `localhost` in `elastcsearch.yml` and `public/index.html` to the IP of your docker VM. Once this is done, use `docker-compose up` to start the example.

## Example

Once you started the docker containers, point your browser to `http://localhost` (or the IP your docker instance runs on).

## FAQ

### Why is ElasticSearch not starting correctly?

If you run the example locally using docker in a virtual machine, you might need to adapt the VM's settings for ElasticSearch to boot. When using boot2docker, these are the commands to update the VM's settings:

```bash
docker-machine ssh default
sysctl -w vm.max_map_count=262144
```
