# Linkoid.Stardew.ModBuildConfig

This is fork of the package [Pathoschild.Stardew.ModBuildConfig](https://www.nuget.org/packages/Pathoschild.Stardew.ModBuildConfig). 
It is intended for advance developers who need more control over the build process,
or only want a subset of the features provided by the original package.


## Using Specific Features of the Package

If only one feature of the package is needed, an Import tag can be used with an SDK and
a Project field specifying a .props or .targets file to only include that feature of the package.
For example, if resolving the `$(GameFolder)` property is all that's needed,
the `FindGameFolder.props` file can be imported by itself.

```xml
<Import Project="FindGameFolder.props" Sdk="Linkoid.Stardew.ModBuildConfig" Version="5.0.0-rc.0" />
```
