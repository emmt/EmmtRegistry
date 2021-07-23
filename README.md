# Registry of my Julia public and private packages

This repository hosts a registry of my Julia packages.

## Usage

To add this registry in Julia:

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
testing](https://en.wikipedia.org/wiki/Continuous_integration):

```julia
using Pkg
Pkg.Registry.add("https://github.com/emmt/EmmtRegistry")
Pkg.Registry.add(RegistrySpec(url = "https://github.com/emmt/EmmtRegistry"))
```
