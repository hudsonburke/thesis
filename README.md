To clone this repository and the submodules it depends on, please use

```shell
git clone --recurse-submodules https://github.com/hudsonburke/thesis.git
```

All code that must interact with the OpenSim Python API should be run in notebooks or scripts separate from a Quarto document.
Otherwise, it will crash the kernel (maybe because of a memory leak), and the Quarto document will not render.