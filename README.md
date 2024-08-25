Introduction
------------

This is a custom build of Proton to fix issues I've had with games. Currently,
only the following fixes are applied:

 - Fix [ENB](http://enbdev.com/download.html) menu not opening when the key input is
    used, and possibly other key input issues.

For most documentation, see the upstream repo at <https://github.com/ValveSoftware/Proton>.


Installation
------------------------

1. Download a release from the [Releases](https://github.com/ceepu45/Proton-ceepufixes/releases)
   page.
2. Create the `~/.steam/root/compatibilitytools.d/` directory if it does not exist.
3. Extract the release to the `~/.steam/root/compatibilitytools.d/` directory.
4. Restart Steam.
5. Go to the properties of the game you want to apply this build to. On the `Compatibility` tab,
   check `Force the use of a specific Steam Play compatibility tool`, and select the desired
   `Ceepu-Proton*` version.

Building from Source
---------------

clone the repo recursively:

```sh
git clone --recurse-submodules https://github.com/ceepu45/Proton-ceepufixes.git
```

Switch to the newly cloned directory and run:
```sh
mkdir build && cd build
../configure.sh --enable-ccache --build-name=<CUSTOM_BUILD_NAME>
make redist
```

Once the build finishes, the `redist` folder can be copied to
`~/.steam/root/compatibilitytools.d/CUSTOM_BUILD_NAME>` to install it. Select it the same as in the
installation instructions.

