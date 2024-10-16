# This is a branch of GCC-14.2 supporting AArch64(Arm64) on Darwin.

The branch is suitable for i686, x86_64 and aarch64 Darwin from Darwin9 (MacOSX 10.5) through Darwin23 (macOS 14 / Sonoma) on architectures relevant to each version.  It should also be applicable to powerpc but has not been tested there.

Please see README for general information on the GCC sources

The GCC 14.2 upstream release has many changes and improvements, please see the general GCC release documentation for details.

Notable additions for macOS/Darwin are:
 * Support for relocatable compiler installations, which restores the ability to carry out uninstalled testing on macOS versions >= 10.11.
 * Support for heap-based trampoline code which is needed for Arm64/AArch64 and is recommended for x86_64 on macOS 11 or later.
 * The addition of `__has_feature/__has_extension` which help to be more compatible with the SDKs.

Please see gcc/config/aarch64/darwinpcs.md for a description of the AArch64 ABI
support.

**_The current release is GCC-14.2-darwin-r2. (October 2024)_**

This release:
 * Contains a number of fixes for compatibility with newer Xcode tools
 * Contains a number of fixes for compatibility with newer SDKs.
 * Adds support for a clang extension where it accepts GNU attributes in a position where they are not allowed by GCC.

**_GCC-14.2-darwin-r0. (August 2024)_**

This release:
 * Updates the fixincludes handling to support newer SDKs better.
 * Recognises -weak_framework in the driver for compatibility with clang.

**_GCC-14.2-darwin-r0. (August 2024)_**

This release:
 * Includes all 14.2 Upstream additions and bug fixes.
 * I've included support for the `availability` attribute in this branch, although this was presented for GCC-14, it did not make it into the upstream release but is an important facility for compatibility with Apple SDKs.

Extras thanks to:
 * 'FX' (https://github.com/fxcoudert) for the main part of the ```__float128``` support, progressing upstream commits and test fixes.

Iain Sandoe, August 2024.

Please report issues for this branch to:
https://github.com/iains/gcc-14-branch/issues
