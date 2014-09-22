# CoApp scripts for LuaJIT via NuGET

Use this package to create NuGet packages that add LuaJIT to your
Visual Studio projects!

## Updating LuaJIT version.
```bash
$ cd luajit-x86
$ git checkout v2.0.3  # or whatever version you want
$ cd ..
$ cd luajit-x64
$ git checkout v2.0.3  # or whatever version you want
$ cd ..
$ vi luajit.autopkg  # change version to match v2.0.3.
$ git commit -m "Updated luajit source to v2.0.3"
$ git submodule update
$ cd luajit-src
$ git status  # make sure the tag matches the version you want
```

## Building LuaJIT NuGet packages.
In VS Developer Console (x86)
```bash
> cd luajit-x86
> cd src
> msvcbuild
```

In VS Developer Console (x64)
```bash
> cd luajit-x64
> cd src
> msvcbuild
```

In Powershell
```bash
> Write-NuGetPackage .\luajit.autopkg
```

## Installing CoApp NuGet helper scripts.
In administrator PowerShell:
```
> Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

In normal PowerShell:
```
> Update-CoAppTools -KillPowershells
```
