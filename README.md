# node-fun-greeter
Sample riff node greeter function to be used with Knative

## create function

```
riff function create node greeter \
  --git-repo https://github.com/trisberg/node-fun-greeter.git \
  --artifact greeter.js \
  --image $USER/node-fun-greeter \
  --env TEST=1
```

## invoke function

```
riff service invoke greeter -- -H 'Content-Type: text/plain' -w '\n' -d world
```
