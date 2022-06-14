# Temperature logger

 Temperature logging from Arduino using Python3. Working with Linux (tested on ArchLinux) and Windows (tested on Windows 10).

## Requirements

* argparse >= 1.4.0

* pyserial >= 3.5

You may install automatically the Python packages using

```bash
pip install -r requirements.txt
```

## Usage

Use

```bash
python temp-logger -h
```

to print the help for the usage.

## Building in Windows

Windows (standalone) executable is built using `pyinstaller`. To reduce the generated file size, it is suggested to create a virtual environment using `venv`.

### Setup the virtual environment

To setup the virtual environment, first go to the source directory and run in the command prompt:

```bash
python -m venv env
```

where `env` is a local folder containing the virtual environment. To activate the create virtual environment run

```bash
cd env/Scripts
activate.bat
cd ../..
```

Finally, install the build requirements using

```bash
pip install -r requirements.txt
pip install -r build_requirements.txt
```

This actually installs `arg-parse` and `pyinstaller` in the created virtual environment. You may use the `pip list` command to take a look at the installed packages.

To exit from the virtual environment (after the building) use

```bash
cd env/Scripts
deactivate.bat
cd ../..
```

### Build the standalone application

To build the standalone application, use in the command prompt

```bash
python build
```
