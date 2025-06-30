# Rust dependency checker

## This script ensure that:
```
Global dependency: Crate specified in the root Cargo.toml and imported with crate.workspace=true
Specific dependency: Crate imported using crate = "x.x.x" (or crate = {version ="x.x.x"})
```

1. Every global dependency used by at least GLOBAL_DEP_THRESHOLD(default 2) package(s)
2. No global dependency is imported as specific dependency
3. Every dependency used by 2 or more packages is a global dependency  
       (no double import which could be bad, I.E different versions)
4. Every dependency of every package is used (no unused imports)

Requirements:  
- rg (https://github.com/BurntSushi/ripgrep)  
- a terminal that accepts ANSI codes  

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
