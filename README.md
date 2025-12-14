# JAX on macOS (Metal) — GPU support

This repository contains quick instructions to install JAX with Metal (GPU) support on macOS.

## Prerequisites
- macOS 12.3+ with Apple Silicon (recommended for Metal support) or a compatible Mac.
- Python 3.8+ installed (system Python or Homebrew-managed).

## Create and activate a virtual environment
Run the following commands in a terminal to create and activate an isolated Python environment:

```bash
python3 -m venv ~/jax-metal
source ~/jax-metal/bin/activate
```

## Install JAX (Metal) and dependencies
Upgrade `pip` and install the minimal dependencies, then install `jax-metal`:

```bash
python -m pip install -U pip
python -m pip install numpy wheel
python -m pip install jax-metal
```

## Verify the installation
Run a quick Python one-liner to verify JAX is importable and working:

```bash
python -c "import jax; import jax.numpy as jnp; print(jnp.arange(10))"
```

If JAX is installed correctly you should see a printed jax array like `DeviceArray([0, 1, ...])` or similar.

## Notes
- If you hit compatibility issues, check the `jax-metal` project README for matching versions and macOS requirements.
- For CPU-only installs on macOS, use the standard `jax` wheels from the official documentation.

## References
- Official JAX documentation: https://github.com/google/jax
- jax-metal: https://github.com/google/jax#apple-m1-metal
