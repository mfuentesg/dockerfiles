## Sassc compiler

This image it is a wrapper for sassc compiler.

### How to use?
```bash
$ docker pull mfuentesg/sassc
$ docker run --volume=/host-dir:/scss mfuentesg/sassc sassc /scss/main.scss > main.css
```

### Available commands

```bash
$ docker run mfuentesg/sassc sassc --help
```
