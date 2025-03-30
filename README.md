# Cookbook - Less is More

### Mkdocs Environment

This site is built with [`mkdocs`](https://www.mkdocs.org/).


Create a Python virtual environment,

```bash
$ python3 -m venv .venv
```

Activate this environment,

```bash
$ source .venv/bin/activate
```

Install `mkdocs` and related packages to the environment.

```bash
$ pip install -U pip

$ pip install -r requirements.txt
```


### Use Mkdocs

* `mkdocs new [dir-name]` - Create a new project, e.g. `mkdocs new .`
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs gh-deploy` - Deploy docs to GitHub pages with `gh-pages` branch.
* `mkdocs -h` - Print help message and exit.

