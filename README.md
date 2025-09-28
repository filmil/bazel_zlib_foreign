# `bazel`-compiled hermetic `zlib`, using `rules_foreign_cc`

[![Publish on Bazel Central Registry](https://github.com/filmil/bazel_zlib_foreign/actions/workflows/publish-bcr.yml/badge.svg)](https://github.com/filmil/bazel_libzstd/actions/workflows/publish-bcr.yml)
[![Publish to my Bazel registry](https://github.com/filmil/bazel_zlib_foreign/actions/workflows/publish.yml/badge.svg)](https://github.com/filmil/bazel_libzstd/actions/workflows/publish.yml)
[![Tag and Release](https://github.com/filmil/bazel_zlib_foreign/actions/workflows/tag-and-release.yml/badge.svg)](https://github.com/filmil/bazel_libzstd/actions/workflows/tag-and-release.yml)
[![Test](https://github.com/filmil/bazel_zlib_foreign/actions/workflows/test.yml/badge.svg)](https://github.com/filmil/bazel_libzstd/actions/workflows/test.yml)

This is a module-compatible version of `zlib` for bazel, but built via the
[`rules_foreign_cc`][rfcc], not via bazel itself.  This is slightly less
efficient, but offers a potentially easier build overall.

You may notice that I have a few similar projects. This is my effort to provide
hermetic libraries for the upcoming Bazel modules world.

Other modules for the samem library may be available. It is not my intention to
check for duplicated effort.

[rfcc]: https://registry.bazel.build/modules/rules_foreign_cc

## Verify the build

```
bazel test //... && cd integration && bazel test //...
```

## Hermeticity

This build is entirely hermetic.


## Release Registry

The project publishes the relevant files to my [personal bazel registry][mcr]
version has not been added to the upstream [BCR][bcr].

This is often the case for pre-release versions.

Add the following to `.bazelrc`:

```
common --registry=https://bcr.bazel.build
common --registry=https://raw.githubusercontent.com/filmil/bazel-registry/main
```


[bcr]: https://registry.bazel.build/
[mcr]: https://github.com/filmil/bazel-registry


