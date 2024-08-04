# Linkoid.Stardew.ModBuildConfig

This is an SDK version of the package [Pathoschild.Stardew.ModBuildConfig](https://www.nuget.org/packages/Pathoschild.Stardew.ModBuildConfig). 
It is intended for advance developers who need more control over the build process,
or only want a subset of the features provided by the original package.

## Using the SDK
To use the SDK, add an Sdk tag inside of the project tag of an MSBuild project file 
to reference a specific vesion of Linkoid.Stardew.ModBuildConfig.
```xml
<Project Sdk="Microsoft.NET.Sdk">
  <Sdk Name="Linkoid.Stardew.ModBuildConfig" Version="1.0.0-rc.0" />
  <!-- ... -->
</Project>
```


## Using Specific Features of the SDK
If only one feature of the SDK is needed, an Import tag can be used with an SDK and
a Project field specifying a .props or .targets file to only include that feature of the SDK.
For example, if resolving the `$(GameFolder)` property is all that's needed,
the `FindGameFolder.props` file can be imported by itself.

```xml
<Import Project="FindGameFolder.props" Sdk="Linkoid.Stardew.ModBuildConfig" Version="1.0.0-rc.0" />
```
