# Docs

Docs are built using [mkdocs](http://www.mkdocs.org)

Look at `build.sh` script to see how it works.

## To Publish New Version

* Update [build.sh](build.sh).
* Update [index.html](index.html) to redirect to the latest version automatically.
* Create a new YAML file, like `5.5.1.yaml` if you are releasing version 5.5.1

## Running Locally

To run the latest version of the docs on [http://127.0.0.1:8000](http://127.0.0.1:8000/quickstart):

```bash
$ ./serve.sh
```

To run a specific version of the docs:

```bash
$ mkdocs serve --config-file 1.3.yaml
```
