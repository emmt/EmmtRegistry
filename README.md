# Registry of my Julia public and private packages

This repository hosts a registry of my Julia packages.


## Installation

Using this registry depends on Julia version.

### Julia versions ≥ 1.1

To add this registry in Julia (version ≥ 1.1, see below for older versions):

```julia
using Pkg
pkg"registry add https://github.com/emmt/EmmtRegistry"
```

If you execute these commands in a fresh Julia installation, you may also want
to add Julia's General Registry with all official packages of Julia.  This can
be done by:

```julia
using Pkg
pkg"registry add General"
```

In a script (e.g., for [CI
testing](https://en.wikipedia.org/wiki/Continuous_integration)):

```julia
using Pkg
Pkg.Registry.add("General")
Pkg.Registry.add(RegistrySpec(url = "https://github.com/emmt/EmmtRegistry"))
```

### Julia versions ≤ 1.0

Move into directory `~/.julia/registries/` and clone this registry:

```sh
cd ~/.julia/registries/
git clone https://github.com/emmt/EmmtRegistry
```

also make sure that you have the `General` (or equivalent) registry, otherwise:

```sh
cd ~/.julia/registries/
git clone https://github.com/JuliaRegistries/General.git
```
