# MyCustomStyleCopAnalyzerPackage

This repo illustrates how to distribute custom rules for StyleCopAnalyzers in the form of a Nuget package, based on the [documentation](https://github.com/DotNetAnalyzers/StyleCopAnalyzers/blob/master/documentation/Configuration.md#sharing-configuration-among-solutions).

This was created to accompany my [introductory blog post](https://blog.markvincze.com/automated-portable-code-style-checking-in-net-core-projects/) about setting up linting for your .NET Core project.

## Usage

If we want to create the package with the `dotnet` CLI, it's important that it doesn't pick up the `nuspec` file automatically, we have to explicitly specify it as an MSBuild argument.

```
dotnet pack -c Release /p:NuspecFile=MyCustomStyleCopAnalyzerPackage.nuspec
```
