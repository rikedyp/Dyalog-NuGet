# Dyalog NuGet
A thin wrapper around the `dotnet` command line interface (CLI) which makes it convenient to depend on NuGet packages from Dyalog APL.

Potential names:
- NuGetConsume
- DyNuGet
- DNuGet
- UsingNuGet
- Dyalog NuGet, but just `NuGet` in the workspace.
## Design
We can establish a namespace in the active workspace which contains metadata from a .NET project which defines a .NET class object.

Adding a package or doing a restore? to a project also does a full `dotnet publish` command to copy into the `nuget-packages` folder.

- Adding a package simply does `dotnet add`, which may download
- When `NuGet.Using` is called, the project is "published". Subsequent calls of `Using` simply have the path to the top-level assembly which is being used.

NuGet targets the project for the version of .NET currently available in the active workspace. A Dyalog forum post states how users can [set the version of .NET being used](https://forums.dyalog.com/viewtopic.php?f=22&t=1863) by Dyalog.

## Usage
```

```


```
NuGet.Setup '/a/project/folder'
NuGet.Add'Clock'
NuGet.Add'Parquet'
```

