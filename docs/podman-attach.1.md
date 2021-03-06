% podman(1) podman-attach - See the output of pid 1 of a container or enter the container
% Dan Walsh
# podman-attach "1" "December 2017" "podman"

## NAME
podman attach - Attach to a running container

## SYNOPSIS
**podman attach [OPTIONS] CONTAINER**

## DESCRIPTION
The attach command allows you to attach to a running container using the container's ID
or name, either to view its ongoing output or to control it interactively.

You can detach from the container (and leave it running) using a configurable key sequence. The default
sequence is CTRL-p CTRL-q. You configure the key sequence using the --detach-keys option

## OPTIONS
**--detach-keys**
Override the key sequence for detaching a container. Format is a single character [a-Z] or
ctrl-<value> where <value> is one of: a-z, @, ^, [, , or _.

**--no-stdin**
Do not attach STDIN. The default is false.

## EXAMPLES ##

```
podman attach foobar
[root@localhost /]#
```
```
podman attach 1234
[root@localhost /]#
```
```
podman attach --no-stdin foobar
```
## SEE ALSO
podman(1), podman-exec(1), podman-run(1)
