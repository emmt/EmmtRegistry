# Registry of my Julia public and private packages

This repository hosts a registry of my Julia packages.

## Usage

To add this registry in Julia:

```julia
using Pkg
Pkg.Registry.add(RegistrySpec(url = "https://github.com/emmt/EmmtRegistry"))
```

or from the Julia's package manager (hit `]` key at Julia's REPL prompt):

```julia
... pkg> registry add https://github.com/emmt/EmmtRegistry
... pkg> registry add General
```

and hit the `Backspace` key at the package manager's prompt to go back to
Julia's REPL.  The `registry add General` command above is needed if you want
to keep Julia's General Registry of official packages (which in general you
want).
