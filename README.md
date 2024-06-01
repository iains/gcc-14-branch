# This is a branch of GCC-14.1 supporting AArch64(Arm64) on Darwin.

The branch is suitable for powerpc, i686, x86_64 and aarch64 Darwin from Darwin9 (MacOSX 10.5) through Darwin23 (macOS 14 / Sonoma) on architectures relevant to each version.

Please see README for general information on the GCC sources

The GCC 14.1 upstream release has many changes and improvements, please see the general GCC release documentation for details.

Notable additions for macOS/Darwin are:
 * Support for relocatable compiler installations, which restores the ability to carry out uninstalled testing on macOS versions >= 10.11.
 * Support for heap-based trampoline code which is needed for Arm64/AArch64 and is recommended for x86_64 on macOS 11 or later.
 * The addition of `__has_feature/__has_extension` which help to be more compatible with the SDKs.

Please see gcc/config/aarch64/darwinpcs.md for a description of the AArch64 ABI
support.

**_The current release is GCC-14.1-darwin-r1. (June 2024)_**

This is a bugfix release; since we now have support for handling the availability attribute, we need to remove the `fixincludes` that corrected missing cases.

**_The current release is GCC-14.1-darwin-r0. (May 2024)_**

This release:
 * Includes all 14.1 Upstream additions and bug fixes.
 * I've included support for the `availability` attribute in this branch, although this was presented for GCC-14, it did not make it into the upstream release but is an important facility for compatibility with Apple SDKs.

Extras thanks to:
 * 'FX' (https://github.com/fxcoudert) for the main part of the ```__float128``` support, progressing upstream commits and test fixes.

Iain Sandoe, May 2024.

Please report issues for this branch to:
https://github.com/iains/gcc-14-branch/issues
