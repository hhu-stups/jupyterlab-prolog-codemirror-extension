# JupyterLab Prolog CodeMirror Extension

A JupyterLab extension providing a Prolog CodeMirror mode based on [extension-cookiecutter-ts](https://github.com/jupyterlab/extension-cookiecutter-ts).

It can be used with a Juypter kernel for Prolog:
- [A Jupyter kernel for SICStus Prolog](https://github.com/anbre/sicstus-prolog-jupyter-kernel)
- [A Jupyter kernel for SWI-Prolog](https://github.com/anbre/swi-prolog-jupyter-kernel)



## Requirements

- JupyterLab >= 3.0

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


The `jlpm` command is JupyterLab's pinned version of
[yarn](https://yarnpkg.com/) that is installed with JupyterLab. You may use
`yarn` or `npm` in lieu of `jlpm` below.

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

### Packaging the extension

See [RELEASE](RELEASE.md)
