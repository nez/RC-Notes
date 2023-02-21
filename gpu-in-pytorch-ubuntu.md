# Setting up Nvidia GPU's to work with PyTorch in Ubuntu

## Verification

To verify that PyTorch can see the GPU's:

```from torch import cuda
cuda.is_available()
```

I also used `gpustat` to see gpu usage.

To install it, run
```pip install gpustat
```

So you can call it with
```gpustat -cp
```

## Nvidia drivers
Install the drivers with
```sudo ubuntu-drivers autoinstall
```
Then reboot and check the result in Python of `cuda.is_available()`.

## Disclaimer:
Before this worked, I installed some nvidia packages with apt, I *think* that `ubuntu-drivers autoinstall` installs everything we need, and if there's anything missing here, please let me know so I can add it to this instructions!
