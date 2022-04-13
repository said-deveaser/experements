##Learning
```bash
npm run concurrently ...
# or, if installed globaly
concurrently ...
```
running script concurrently
```bash
    concurrently "command1 args" "command2 args?" # run commands concurrently  
```

```console
[0] result command1
[1] result command2
[0] exit code 0
[1] exit code 1
```

named command in console
```bash
    concurrently -n first-command-name,second-command-name "command1 args" "command2 args?" # run commands concurrently  
```

```console
[first-command-name] result command1
[second-command-name] result command2
[first-command-name] exit code 0
[second-command-name] exit code 1
```
NPM run commands can be shortened:
```bash
concurrently "npm:watch-js" "npm:watch-css" "npm:watch-node"

# Equivalent to:
concurrently -n watch-js,watch-css,watch-node "npm run watch-js" "npm run watch-css" "npm run watch-node"
```
