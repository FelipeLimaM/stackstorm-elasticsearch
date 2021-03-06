# System Tests

Before executing `st2.sh`, ensure that ELK is installed, configured and running on host `elk`.

Before executing `st2-nohost.sh`, ensure that ELK is installed, configured and running. The pack-level configuration should specify the ELK host.

If you do not already have an ELK stack available, the quickest way to run one is:

```bash
git clone github.com:stackstorm/st2-docker
```

Add the following service to `st2-docker/docker-compose.yml`

```yaml
elk:
  image: sebp/elk:latest
  container_name: elk
  networks:
    - private
```

Then follow the `st2-docker` [README](https://github.com/StackStorm/st2-docker/blob/master/README.md).
