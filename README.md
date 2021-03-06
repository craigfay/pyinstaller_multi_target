
# About

An example of using GitHub actions to build multi-platform executable files from python scripts. 

# Structure
* `example.py` The python module that will be compiled
* `.github/workflows/build_exe.yml` The github actions config that allows the build to be triggered.

# Why Not Cross Compile? 
Another way to solve the same problem would be to use a single OS (say, Ubuntu) to install all the required build tools. In addition to the normal Python tools, the list ould include [toolchains](https://elinux.org/Toolchains) specifically suited to cross-compiling between the host machine and each target. This is necessary in part because each OS uses a different C Standard Library. [Rust Cross](https://github.com/japaric/rust-cross) provides a great summary of the details. Instead, this example favors using [Virtual Environments](https://github.com/actions/virtual-environments), which are well supported by GitHub actions, and arguably less complex.
