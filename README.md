# Rust dependency checker

## Installation

Download it to your current projet's scripts directory (make sure you have a `./scripts` directory)
```console
curl https://raw.githubusercontent.com/Bowarc/rust_dependency_checker/refs/heads/main/dependency_checker.py -o./scripts/dependency_checker.py
```

## Usage
When in your rust projet's root directory
```console
python ./scripts/dependency_checker.py
```

## Notes
I knowingly do not use any toml parsing library as I do not want this script to depend on python library not installed by default
