Sometimes you want to poll multiple processes, and wait until they complete. But you want to see a progressbar in cli.

Let say 

## Install

```
curl -L https://github.com/lalyos/pollprogress/releases/download/v0.1.0/pollprogress_0.1.0_$(uname)_x86_64.tgz | tar -xz -C /usr/local/bin/
```

## Usage

```
pollprogress check.yml
```

## Config file syntax

Its quite simlpe each process/task define its name, and the shell command to check the progress
```
processA: curl https://some.api.io/longprocess1/status | jq .progress
processB: curl https://some.api.io/longprocess2/status | jq .progress
processC: curl https://some.api.io/longprocess3/status | jq .progress
```

The command should print the progress to STDOUT in a format : **<actual>/<total>**

## License

MIT
