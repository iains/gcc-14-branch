# This is a branch of GCC-14.4 supporting AArch64(Arm64) on Darwin.

The branch is suitable for i686, x86_64 and aarch64 Darwin from Darwin9 (MacOSX 10.5) through Darwin25 (macOS 26 / Tahoe) on architectures relevant to each version.  It should also be applicable to powerpc but has only been tested using
Rosetta on MacOSX 10.5.

Please see README for general information on the GCC sources

Please see gcc/config/aarch64/darwinpcs.md for a description of the AArch64 ABI
support.

**_The current release is GCC-14.4-darwin-r0. (June 2026)_**

This release:
 * Includes all 14.4 Upstream additions and bug fixes.
 * Contains a number of fixes for compatibility with newer Xcode tools
 * Contains a number of fixes for compatibility with newer SDKs.

Extras thanks to:
 * 'FX' (https://github.com/fxcoudert) for the main part of the ```__float128``` support, progressing upstream commits and test fixes.

Iain Sandoe, June 2026.

Please report issues for this branch to:
https://github.com/iains/gcc-14-branch/issues
