# pyrpl-lite-env
Installation of the environnement in the redpitaya for pyrpl-lite.
This Makefile clones cpython git in ./build and pyrpl-lite git in ~/ folder.
It proced to the compilation/installation of python 3.5.10, then install the system packed scipy and proced to the installation/compilation of the pip packages necessary to pyrpl.

# Pre-installation
You can either just copy this Makefile on the redPitaya in your chosen folder or clone this git repository or download it directly from GitHub :
```bash
cd ~/;
mkdir pyrpl-lite-env && cd $_;
curl -O https://raw.githubusercontent.com/samlekebab/pyrpl-lite-env/release/Makefile;
```

# Install the environnement
In the folder containing the makefile, run the command :
```
make
```
(note that we are using the root user of the redPitaya to do the installation)

# Cleanup
To clean after the installation and remove build files (cpython repo) :
```
make cleanBuild
```

If you want to redo the installation in a clean environement (beware it might suppress your own installation made with or without this Makefile, including the pyrpl repo, and your local changes to it)
```
make clean
```
Finer-grained cleanning targets can be seen in the Makefile.
