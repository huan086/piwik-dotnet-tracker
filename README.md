# Piwik C# Tracking API

This is the official C# implementation of the [Piwik Tracking API](http://piwik.org/docs/tracking-api/).

Check the [release page](https://github.com/piwik/piwik-dotnet-tracker/releases)
for supported versions of Piwik.

## Usage

Three Visual Studio Solutions are provided : 

* [Piwik.Tracker.sln](Piwik.Tracker.sln) : Library project
* [Piwik.Tracker.Samples.sln](Piwik.Tracker.Samples.sln) : Console Samples project
* [Piwik.Tracker.Web.Samples.sln](Piwik.Tracker.Web.Samples.sln) : ASP.NET Samples project

The two Samples projects provide exhaustive examples.

## How to contribute

The Piwik C# Tracking API is a translation of the [official PHP Tracking API](https://github.com/piwik/piwik/tree/master/libs/PiwikTracker) in C#.

Translating the project is currently a manual process.

Manually translating the project is tedious because it requires

* identifying features that have already been translated
* merging code

We would ideally like to automate this process, we welcome contributions aimed towards this goal.

To ease the process in the mean time, the following rules are applied to any new code contributions :

* one-to-one commit mappings between the PHP and C# projects
* the C# code should mirror as close as possible the PHP code

As long as we do not have an automated process, we welcome suggestions in improving the manual process.

### Code style

To mirror as close as possible the PHP code, we copy-paste the PHP code in the C# class and alter it so it compiles.

This can lead in a loss of C# best practices. We consider the time savings an acceptable trade-off.

### Tagging

We would ideally have liked to keep a one-to-one tag mapping between the PHP and C# projects.

However, the PHP tracking API source code can be tagged redundantly because

* the PHP tracking API is not separate from the main Piwik repository
* the tracking API does not require updates for each version of Piwik

To avoid creating redundant tags, we only keep tags that have introduced changes in the source code.

Here is a command example to list changes between two versions of Piwik:

    git log 1.5.1..1.6 libs/PiwikTracker/PiwikTracker.php


# [License](LICENSE)