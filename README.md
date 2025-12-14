### Mac OS JAX installation with GPU support
python3 -m venv ~/jax-metal
source ~/jax-metal/bin/activate
python -m pip install -U pip
python -m pip install numpy wheel
python -m pip install jax-metal
### Installation verification
python -c 'import jax; print(jax.numpy.arange(10))'
