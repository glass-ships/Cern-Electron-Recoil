# Cern-Electron-Recoil

| [Documentation](https://glass-ships.github.io/cern-electron-recoil) |

An example project using monarch ingest cookiecutter.

## Requirements

- Python >= 3.10
- [Poetry](https://python-poetry.org/docs/#installation)

## Starting a new project

Upon creating a new project from the `cookiecutter-monarch-ingest` template, you can install and test the project:

```bash
cd Cern-Electron-Recoil
make install
make test
```

To finish setting up this project:

1. Edit the `download.yaml`, `transform.py`, `transform.yaml`, and `metadata.yaml` files to suit your needs.
   - For more information, see the [Koza documentation](https://koza.monarchinitiative.org) and [kghub-downloader](https://github.com/monarch-initiative/kghub-downloader).
1. Add any additional dependencies to the `pyproject.toml` file.
1. Adjust the contents of the `tests` directory to test the functionality of your transform.
1. Update this `README.md` file with any additional information about the project.
1. Add any appropriate documentation to the `docs` directory.

Once you have completed these steps, you can remove this section from the `README.md` file.

## Installation

```bash
cd Cern-Electron-Recoil
make install
# or
poetry install
```

> **Note** that the `make install` command is just a convenience wrapper around `poetry install`.

Once installed, you can check that everything is working as expected:

```bash
# Run the pytest suite
make test
# Download the data and run the Koza transform
make download
make run
```

## Usage

This project is set up with a Makefile for common tasks.  
To see available options:

```bash
make help
```

### Download and Transform

Download the data for the cern_electron_recoil transform:

```bash
poetry run cern_electron_recoil download
```

To run the Koza transform for Cern-Electron-Recoil:

```bash
poetry run cern_electron_recoil transform
```

To see available options:

```bash
poetry run cern_electron_recoil download --help
# or
poetry run cern_electron_recoil transform --help
```

---

> This project was generated using [monarch-initiative/cookiecutter-monarch-ingest](https://github.com/monarch-initiative/cookiecutter-monarch-ingest).  
> Keep this project up to date using cruft by occasionally running in the project directory:
>
> ```bash
> cruft update
> ```
>
> For more information, see the [cruft documentation](https://cruft.github.io/cruft/#updating-a-project)
