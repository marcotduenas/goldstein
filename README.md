# Goldstein
> Big brother is watching you!
<img src="./img/goldstein.png" width= 300px alt="Goldstein" align="right"/>


**Goldstein** is an simple and low-level package manager. It was written entirely in shell script and tries to be portable as much as possible.

# Installation
```bash
git clone https://github.com/marcotduenas/goldstein
cd goldstein
chmod +x install
sudo ./install
```
# Basic usage for creating a package
1. Get source code of the software you want.
2. Extract it.
3. Make sure to configure, set the prefix as **/usr**.
4. Create a fakeroot dir in /tmp. Example: mdkir /tmp/nano
5. make && make install the package to the fakeroot dir. Example: make && make instal DESTDIR=/tmp/nano
6. Go to the fakeroot dir and check if there are two folders (data & usr)
7. Use goldstein-create to create your .gds package. Example: goldstein-create -c nano-7.2-1.gds. **IMPORTANT!** make sure to follow the pattern *'pkgname-version-build.gds'*
8. cd ../ and then goldstein-install your .gds package. Example goldstein-install nano-7.2.1.gds.

# Basic usage for installing and removing a package a package already built
## Installing
```
goldstein-install [package.gds]. Example: goldstein-install nano-7.2-1.gds
```
## Removing
```
goldstein-remove [packagename]. Example: goldstein-remove nano
```
# Customization
Just edit the source code.
