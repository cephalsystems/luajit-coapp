# NuGet native package builder for LuaJIT

Use this package to create NuGet packages to include LuaJIT in your
Visual Studio projects!

## Updating LuaJIT version.
'''bash
$ cd luajit-src
$ git checkout v2.0.3  # or whatever version you want
$ cd ..
$ vi luajit.autopkg  # change version to match v2.0.3.
$ git commit -m "Updated luajit source to v2.0.3"
$ git submodule update
$ cd luajit-src
$ git status  # make sure the tag matches the version you want
'''

## Building LuaJIT NuGet package
In VS Developer Console
'''bash
> cd luajit-src
> cd src
> msvcbuild
'''
In Powershell
'''bash

'''

## Installing CoApp NuGet helper scripts.
In administrator PowerShell:
'''
> Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
'''

In normal PowerShell:
'''
> Update-CoAppTools -KillPowershells
'''
