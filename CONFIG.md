# Config

Adding another ReVanced app is as easy as this:
```toml
[App Name]
apkmirror-dlurl = "https://www.apkmirror.com/apk/inc/app"
# or uptodown-dlurl = "https://app.en.uptodown.com/android"
# or apkmonk-dlurl = "https://www.apkmonk.com/app/com.app.app/"
```

## More about other options:

There is existing example below with all defaults shown and all the keys explicitly set.  
**All keys are optional** (except for download urls) and are assigned to their default values if explicitly is not set.  

```toml
parallel-jobs = 1
# Amount of cores to use for parallel patching, if not set nproc is used
patches-source = "inotia00/revanced-patches"
# Where to fetch patches bundle from ― default: "anddea/revanced-patches"
integrations-source = "inotia00/revanced-integrations"
# Where to fetch integrations from ― default: "anddea/revanced-integrations"
cli-source = "j-hc/revanced-cli"
# Where to fetch cli from ― default: "j-hc/revanced-cli"
# options like cli-source can also set per app
rv-brand = "ReVanced eXtended"
# Rebrand from 'ReVanced eXtended' to something different ― default: "ReVanced eXtended"

patches-version = "v2.111.4"
# Use specific patches version ― default: latest available
integrations-version = "v0.42.1"
# Use specific integrations version ― default: latest available
cli-version = "v3.0.1"
# Use specific CLI version ― default: latest available

[App Name]
app-name = "App"
# If set, release name becomes App instead of Some-App ― default is same as table name, which is 'App'
enabled = true
# Whether to build the app ― default: true
version = "auto"
# 'auto', 'latest', 'beta' or a custom one e.g. '17.45.36' ― default: auto
# 'auto' option gets the latest possible version supported by all the included patches
# 'latest' gets the latest stable without checking patches support
# 'beta' gets the latest beta/alpha
include-stock = true
# includes stock apk in the module, default: true
build-mode = "apk"
# 'both', 'apk' or 'module' ― default: apk
excluded-patches = "'Some Patch' 'Some Other Patch'"
# Whitespace seperated list of patches to exclude
included-patches = "'Some Patch' 'Some Other Patch'"
# Whitespace seperated list of patches to include, all default patches are included by default
exclusive-patches = false
# Exclude all patches by default ― default: false
apkmirror-dlurl = "https://www.apkmirror.com/apk/inc/app"
uptodown-dlurl = "https://app.en.uptodown.com/android"
apkmonk-dlurl = "https://www.apkmonk.com/app/com.app.app/"
module-prop-name = "app-magisk"
# Magisk module prop name.
apkmirror-dpi = "360-480dpi"
# Used to select apk variant from apkmirror ― default: nodpi
apkmirror-arch = "arm64-v8a"
# 'arm64-v8a', 'arm-v7a', 'all', 'both'. 'both' downloads both arm64-v8a and arm-v7a ― default: all
```

# Building ReVanced
Use the [original project](https://github.com/AbakNacchan/revanced-magisk-module) instead.
