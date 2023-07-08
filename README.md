# PyO3 + setuptools-rust blueprint

An example of a basic Python extension module built using PyO3 and [`setuptools_rust`](https://github.com/PyO3/setuptools-rust).

## Building and Testing

To build this package, make sure your pip is up-to-date, and install build package as well:

```shell
pip3 install -U build pip
```

To build and test use `python -m pip install -e .`:

```shell
python3 -m build -s -w --outdir dist
pip3 install -r requirements-dev.txt
python3 -m pip install -e . && python3 -m pytest
```

## Copying this example

Use [`cargo-generate`](https://crates.io/crates/cargo-generate):

```bash
cargo install cargo-generate
cargo generate --git https://github.com/PyO3/pyo3 examples/setuptools-rust-starter
```

(`cargo generate` will take a little while to clone the PyO3 repo first; be patient when waiting for the command to run.)
