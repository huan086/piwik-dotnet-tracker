# Piwik C# Tracking API [![Build Status](https://travis-ci.org/piwik/piwik-dotnet-tracker.svg?branch=master)](https://travis-ci.org/piwik/piwik-dotnet-tracker)

This is the official C# implementation of the [Piwik Tracking API](http://piwik.org/docs/tracking-api/).

## Usage

Three Visual Studio Solutions are provided : 

* [Piwik.Tracker.sln](Piwik.Tracker.sln) : Library project
* [Piwik.Tracker.Samples.sln](Piwik.Tracker.Samples.sln) : Console Samples project
* [Piwik.Tracker.Web.Samples.sln](Piwik.Tracker.Web.Samples.sln) : ASP.NET Samples project

## Changelog

Pending [#22](../../issues/22)

## Publishing the project to NuGet

### Requirements

1. The process detailed in this section must be executed right before adding a
   release tag to git.
2. Publishing the project to NuGet must be done by a member of the Piwik team,
   holder of the private NuGet Key.

### Steps

1. Validate tests (requires #7)
2. Update and commit `AssemblyInfo.cs` with new version
3. Create git tag
4. Build the project using the Release solution configuration
5. Create NuGet packages using `nuget pack Piwik.Tracker\Piwik.Tracker.csproj -Prop Configuration=Release -Symbols`
6. Publish packages using `nuget push Piwik.Tracker.VERSION.nupkg`

# [License](LICENSE)
