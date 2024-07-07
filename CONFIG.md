# Config

Adding another RV-X app is as easy as this:
```toml
[App Name]
apkmirror-dlurl = "https://www.apkmirror.com/apk/inc/app"
```

## More about other options:

There is existing example below with all the default values shown and all the keys explicitly set.
Except for download URL, **all keys are optional** and are assigned to their default values if explicitly is not set.
Note that this extensive builder is using `latest patches` available by default, not the `pre-release` one.

```toml
parallel-jobs = 1
# Amount of cores to use for parallel patching, if not set nproc is used
patches-source = "anddea/revanced-patches"
# Where to fetch patches bundle from ― default: "anddea/revanced-patches"
integrations-source = "anddea/revanced-integrations"
# Where to fetch integrations from ― default: "anddea/revanced-integrations"
cli-source = "inotia00/revanced-cli"
# Where to fetch cli from ― default: "inotia00/revanced-cli"
# Options like `patches-source`, `integrations-source`, and `cli-source` can also set per app
rv-brand = "RV-X"
# Rebrand from 'RV-X' to something different ― default: "RV-X"

patches-version = "v2.111.4"
# Use specific patches version ― default: latest release
integrations-version = "v0.42.1"
# Use specific integrations version ― default: latest release
cli-version = "v3.0.1"
# Use specific CLI version ― default: latest release

[App Name]
app-name = "App"
# If set, release name becomes `App` instead of `App Name` ― default is same as table name, which is `App Name`
enabled = true
# Whether to build the app ― default: true
version = "auto"
# `auto`, 'latest', 'beta' or a custom one e.g. `17.45.36` ― default: auto
# `auto` option will get you the latest possible version supported by the sources
# `latest` will get you the latest stable version without checking sources support
# `beta` is similar as 'latest', but in beta version
include-stock = true
# includes stock apk in the module, default: true
build-mode = "apk"
# `both`, `apk` or `module` ― default: apk
excluded-patches = "'Patches' 'Any Other Patches'"
# Whitespace separated list of patches to exclude
included-patches = "'Patches' 'Any Other Patches'"
# Whitespace separated list of patches to include, all default patches are included by default
exclusive-patches = false
# Exclude all patches by default ― default: false
apkmirror-dlurl = "https://www.apkmirror.com/apk/inc/app"
module-prop-name = "app-magisk"
# Magisk module prop name.
apkmirror-dpi = "360-480dpi"
# Used to select apk variant from apkmirror ― default: nodpi
apkmirror-arch = "arm64-v8a"
# `arm64-v8a`, `arm-v7a`, `all`, `both`. `both` downloads both arm64-v8a and arm-v7a ― default: all
```

# Building RV
Use the [original project](https://github.com/AbakNacchan/RV) instead.
