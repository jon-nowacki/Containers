# Containers
Build with

```
export SINGULARITY_CACHEDIR=/date/temp
sudo time singularity build ubuntu_mamba_base.simg singularity.recipe
```

Should take about 2 minutes with just mamba, 4 minutes with conda

Run with

```
singularity shell ubuntu_mamba_base.simg
```


Build with
```
time singularity build bifics.simg bifics.recipe
```




