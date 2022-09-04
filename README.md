#   eggolib's Documentation

This repository is used for managing eggolib's documentation site.

<br>


## Contributing

First, you'll need to install [mike](https://github.com/jimporter/mike), a Python utility used for deploying multiple versions of eggolib's documentation site:

```python
pip install mike
```
<br>

Then, you can fork the repository and clone your fork locally with `git clone <repo>`. You can then make changes to the files inside your fork.
*(For example, let's say that you've forked the repository and your username is `generic-username123`)*

```
git clone https://github.com/generic-username123/eggolib.github.io
```
<br>

To view your changes, you'll have to deploy it locally with `mike deploy <version>` before serving it on `http://localhost:8000` with `mike serve`:

```python
mike deploy 1.2.x

mike serve
```
