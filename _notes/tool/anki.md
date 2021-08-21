---
doc: https://github.com/ankitects/anki/blob/main/docs/development.md
update: 2021-08-21
---

## Build locally

Firstly clone anki repository from
[here](https://github.com/ankitects/anki)

### Install bazel

Anki requires a specific bazel version.
Check the required bazel version with:

```shell
cat .bazelversion
```

If the required bazel version is, for example, 4.0.0,
download `bazel-4.0.0-linux-x86_64` manually at the
[bazel release page](https://github.com/bazelbuild/bazel/releases/tag/4.0.0).
Then move it to your bin folder:

```shell
mv ~/Downloads/bazel-4.0.0-linux-x86_64 ~/.local/bin/bazel
```

To download from the command line, instead, use:

```shell
curl --location --output ~/.local/bin/bazel "https://github.com/bazelbuild/bazel/releases/download/4.0.0/bazel-4.0.0-linux-x86_64"
```

Finally add execution permission to the binary:

```shell
chown u+x ~/.local/bin/bazel
```

### Build and install anki

At least python 3.8 is required.

```shell
./scripts/build
pip install --user --upgrade pip
pip install --user --upgrade bazel-dist/*.whl
```

Anki then can be executed by typing `anki` on the terminal.

### Enable Fcitx support

Find the system's and Anki's `platforminputcontexts` directory with `find`
and symlink fcitx plugin.

```shell
ln -s /usr/lib/qt/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so ~/.local/lib/python3.9/site-packages/PyQt5/Qt5/plugins/platforminputcontexts/libfcitxplatforminputcontextplugin.so
```
