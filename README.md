# JupyterLab Prolog CodeMirror Extension

A JupyterLab extension providing a Prolog CodeMirror mode.

Based on [extension-cookiecutter-ts](https://github.com/jupyterlab/extension-cookiecutter-ts).


## Requirements

- JupyterLab >= 3.1

## Install

To install the extension, execute:

```bash
pip install jupyterlab_prolog_codemirror_extension
```

## Uninstall

To remove the extension, execute:

```bash
pip uninstall jupyterlab_prolog_codemirror_extension
```

## Contributing

### Development install

Notes:
- You will need NodeJS to build the extension package.
- A TypeScript version < 4.4.0 is required. It can be installed with `npm install typescript@4.1.3`


The `jlpm` command is JupyterLab's pinned version of [yarn](https://yarnpkg.com/) that is installed with JupyterLab. You may use `yarn` or `npm` in lieu of `jlpm` below.

```bash
# Clone the repo to your local environment
# Change directory to the jupyterlab_prolog_codemirror_extension directory
# Install package in development mode
pip install -e .
# Link your development version of the extension with JupyterLab
jupyter labextension develop . --overwrite
# Rebuild extension Typescript source after making changes
jlpm build
```

You can watch the source directory and run JupyterLab at the same time in different terminals to watch for changes in the extension's source and automatically rebuild the extension.

```bash
# Watch the source directory in one terminal, automatically rebuilding when needed
jlpm watch
# Run JupyterLab in another terminal
jupyter lab
```

With the watch command running, every saved change will immediately be built locally and available in your running JupyterLab. Refresh JupyterLab to load the change in your browser (you may need to wait several seconds for the extension to be rebuilt).

By default, the `jlpm build` command generates the source maps for this extension to make it easier to debug using the browser dev tools. To also generate source maps for the JupyterLab core extensions, you can run the following command:

```bash
jupyter lab build --minimize=False
```

### Development uninstall

```bash
pip uninstall jupyterlab_prolog_codemirror_extension
```

In development mode, you will also need to remove the symlink created by `jupyter labextension develop`
command. To find its location, you can run `jupyter labextension list` to figure out where the `labextensions`
folder is located. Then you can remove the symlink named `jupyterlab_prolog_codemirror_extension` within that folder.

### Upload to PyPI

This extension is available as a Python package on the [Python Package Index](https://pypi.org/). A new version of the package can be published in the following way:
1. Install the requirements build and twine:
  `pip install build twine`
2. Increase the version in [package.json](./package.json)
3. Create the distribution files:
  `python -m build`
4. Upload the package to PyPI:
  `twine upload dist/*`

For further information, see the [Packaging Python Projects Tutorial](https://packaging.python.org/en/latest/tutorials/packaging-projects/).
