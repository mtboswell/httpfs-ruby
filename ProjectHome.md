httpfs-ruby mounts a directory mount-point and allow you to read any http file as it they were local.

This is based on [fusefs](http://rubyforge.org/projects/fusefs/), a fuse binding for ruby.
It is a one-day hack so it seems to works but should be considered beta. (btw im still amazed that it is now possible to write a filesystem in 125-lines :)

Usage:
1. mount the httpfs mount point
```
httpfs your/mount/point
```
2. read http file thru it, e.g. say http://example.com/index.html
```
cat your/mount/point/example.com/index.html
```

# Notes #
As the name indicates this is coded in ruby, so dont expect it to be cpu efficient. This is a one day hack, published in case some people find it helpfull.
  * [httpfs](http://httpfs.sourceforge.net/) is coded in C so is much likely more cpu efficient, but it allows only to mount a single file per mount. It didnt fit my need.

# Credits #
  * [fusefs](http://rubyforge.org/projects/fusefs/) is the ruby library that httpfs-ruby uses to access fuse feature. 'FuseFS lets ruby programmers define filesystems entirely in Ruby' from the project homepage.