## logstash-tester
Just simple local tester for logstash configuration.
Uses [flog](https://github.com/mingrammer/flog) for fake log generation.

### Usage
```sh
docker compose up -d
docker compose down
```

### check sincedb
```sh
# attach to logstash container
$ cd /usr/share/logstash/data/plugins/inputs/file
$ ls -a | grep sincedb
.sincedb_e96a7e74e288b15666f4a10a4fb6a092

$ ls -a | grep since | xargs cat
12 0 45 28967 1710771112.1678162 /log/generated.log
```
