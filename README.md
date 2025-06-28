# wayland-headers packaged for the Zig build system

This is a Zig package which provides various Wayland headers needed to develop and cross-compile.

It includes:

* non-generated Wayland headers (see `wayland/`)

* generated headers for Wayland protocols (see `wayland-protocols/`):

  * fractional-scale-v1
  * idle-inhibit-unstable-v1
  * pointer-constraints-unstable-v1
  * relative-pointer-unstable-v1
  * viewporter
  * xdg-activation-v1
  * xdg-decoration-unstable-v1
  * xdg-shell

* And headers for libdecor (see `libdecor/`)

This was once maintained by Mach Engine, but was abandoned and moved to a personal repository, which was then deleted. This is a reupload, pulled from [https://pkg.machengine.org/wayland-headers/7c53e7483c3cfb5c6780ae542c9f5cfa712a826a.tar.gz](https://pkg.machengine.org/wayland-headers/7c53e7483c3cfb5c6780ae542c9f5cfa712a826a.tar.gz) and modified to build for latest GLFW and zig.

## Updating

To update this repository, run `./update.sh` followed by `./verify.sh` to verify the repository contents.

## Verifying repository contents

For supply chain security reasons (e.g. to confirm we made no patches to the code) we provide a `git diff` command you can run to verify the contents of this repository:

```sh
./verify.sh
```

If nothing is printed, there is no diff. Deleted files, and changes to `README.md`, `build.zig`, `.github` CI files and `.gitignore` are ignored.

## Issues

Issues are tracked in the [main Mach repository](https://github.com/hexops/mach/issues?q=is%3Aissue+is%3Aopen+label%3Awayland-headers).
