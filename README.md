# A CUDA based ed25519 vanity key finder (in Base58)

This is a GPU based vanity key finder. It does not currently use a CSPRNG and
any key generated by this tool is 100% not secure to use. Great fun for Tour de
Sol though.

## Configure
Open `src/config.h` and add any prefixes you want to scan for to the list.

## Building
Make sure your cuda binary are in your path, and build:

```bash
$ export PATH=/usr/local/cuda/bin:$PATH
$ make -j$(nproc)
```

## Running

```bash
LD_LIBRARY_PATH=./src/release ./src/release/cuda_ed25519_vanity
```
