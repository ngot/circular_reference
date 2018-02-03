# Circular Reference

Circular reference in Node.js and Fibjs.

## Node.js

Just a note here. 🤣🤣🤣

node a.js

```shell
a1
b1
a is: {}
b2
b is: bbb
a2
```

## Fibjs

It is different in fibjs.

Let's have a look at the log:

fibjs a.js

```shell
a1
b1
a1
b is: {}
a2
a is: aaa
b2
b is: bbb
a2
```

It's because fibjs has the `run` mechanism which is different from Node.js.Fibjs won't cache the run entry file.

If you use `c.js` to bootstrap the program, the behavior will be the same.

fibjs c.js

```shell
a1
b1
a is: {}
b2
b is: bbb
a2
```
