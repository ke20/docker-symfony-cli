# symfony-cli

A lightweight image with symfony-cli

Add in your shell rc file the code below :
```shell
symfony () {
    tty=
    tty -s && tty=--tty
    docker run $tty -i --rm \
        -v $(pwd):$(pwd) \
        -v /etc/passwd:/etc/passwd:ro \
        -v /etc/group:/etc/group:ro \
        -u $(id -u):$(id -g) \
        -v "$(pwd):$(pwd)" \
        -w "$(pwd)" \
        ke20/symfony-cli "$@"
}
```

Open a new terminal or reload your shell session and the command below should succeed:

```shell
$ symfony --help
```
