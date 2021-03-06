[![Build Status](https://travis-ci.org/Naruto/simon-speck-net.svg?branch=develop)](https://travis-ci.org/Naruto/simon-speck-net?branch=develop)
[![NuGet version](https://badge.fury.io/nu/simonspecknet.svg)](https://badge.fury.io/nu/simonspecknet)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FNaruto%2Fsimon-speck-net.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FNaruto%2Fsimon-speck-net?ref=badge_shield)
# simon-speck-net

c# binding of [Naruto/simon-speck-c](https://github.com/Naruto/simon-speck-c)


# development
## preapre

- mono
- Unity (if create unity package)

## get source

```bash
git clone --recursive git@github.com:Naruto/simon-speck-net.git
```

## build

build simon-speck-net and nunit test.

```bash
cd /path/to/simon-speck-net
cd ./net
mono .nuget/nuget.exe restore
xbuild /p:TargetFrameworkVersion="v4.5" /p:Configuration=Release
mono ./packages/NUnit.ConsoleRunner.3.7.0/tools/nunit3-console.exe ./speckTest/bin/Release/speckTest.dll
```

or

```bash
cd /path/to/simon-speck-net
./scripts/build.sh
```

## create nuget package

```bash
cd /path/to/simon-speck-net
./scripts/create_nuget.sh
```

SimonSpeckNet nuget package file is outputted to `out/net` directory.

## create unity package

```bash
cd /path/to/simon-speck-net
./scripts/create_unitypackage.sh
```

SimonSpeckNet unitypackage file is outputted to `out/unity` directory.


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FNaruto%2Fsimon-speck-net.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FNaruto%2Fsimon-speck-net?ref=badge_large)