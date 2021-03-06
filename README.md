# ATLauncher
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FDev-Osmium%2FATLauncher.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FDev-Osmium%2FATLauncher?ref=badge_shield)


## What is it?

ATLauncher is a Launcher for Minecraft which integrates multiple different ModPacks to allow you to download and install
ModPacks easily and quickly.

## Links

* [ATLauncher Website](https://www.atlauncher.com)
* [ATLauncher Facebook](http://www.facebook.com/ATLauncher)
* [ATLauncher Reddit](http://www.reddit.com/r/ATLauncher)
* [ATLauncher Twitter](http://twitter.com/ATLauncher)

## Coding Standards & Styling Guidelines

Please see the [STYLE.md](STYLE.md) file for coding standards and style guidelines.

## Contributing to ATLauncher

If you wish to contribute to ATLauncher in any way, take a look at [CONTRIBUTING.md](CONTRIBUTING.md)

## Testing

Please see the [TESTING.md](TESTING.md) file for information on how we write tests.

## Building

### Windows

#### Requirements

##### Java Development Kit (JDK)

Download and install the latest version from
[Oracle's Java Downloads page](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html).

##### Apache Maven

Download Apache Maven via the official [download site](http://maven.apache.org/download.cgi).

Make sure to follow the [installation docs](http://maven.apache.org/install.html).

##### launch4j

Download and install [launch4j](http://sourceforge.net/projects/launch4j/files/launch4j-3/3.1.0-beta2/).

Make sure to add the directory containing launch4jc to your executable path which for me on 64bit Windows was:

```
`C:\Program Files (x86)\Launch4j`
```

## Running the application

If you wish to run the application in development, you can run the following:

```
mvn exec:java
```

All working files will be put in the `testDir` directory.

## Building artefacts

To build artefacts for release, simply run `mvn install`.

## Plugging In Your Data

To get started with the code and plug in your own data, you need to edit the
/src/main/java/com/atlauncher/data/Constants.java file.

By using this source code you don't get permissions to use our CDN/files/assets/modpacks. See the License section at the
bottom for more.

See below for explanations as to what each constant means.

### VERSION

This is a LauncherVersion object passed in the reserved, major, minor, revision ints for this version of the launcher.
See the 'Versioning System' section below.

### API_BASE_URL

This is a link to your server side API for processing of leaderboard times and pack installs. This is optional and can
be removed. We do not give implementation code, this is your own doing.

### PASTE_CHECK_URL

This is a link to the url where an instance of [stikked](https://github.com/claudehohl/Stikked) is running (For instance
http://www.mypaste.com) this is how the launcher knows if the paste was successful by checking the response from the API
for the url of the software.

_Please note that the domain given above IS NOT REAL. You must install [stikked](https://github.com/claudehohl/Stikked)
on your own domain and reference it, the domain is only there as an example of what a valid value is._

### PASTE_API_URL

This is a link to the create api command for the instance of [stikked](https://github.com/claudehohl/Stikked) is running
(For instance http://www.mypaste.com/api/create/)

_Please note that the domain given above IS NOT REAL. You must install [stikked](https://github.com/claudehohl/Stikked)
on your own domain and reference it, the domain is only there as an example of what a valid value is._

### SERVERS

This is an array of
[Server](https://github.com/ATLauncher/ATLauncher/blob/master/src/main/java/com/atlauncher/data/Server.java) type
elements the launcher uses as a base to download files.

### LAUNCHER_NAME

This is the name of the launcher.

### How to make your data

To make the data the Launcher needs you will need to figure out your own server side way of doing that. You can create a
system to do it automatically or you can manually do it by just popping the files on the server. The best way to get the
file structure and contents is to examine the source code and the ATLauncher files it downloads.

## Versioning System

Starting with version 3.2.1.0 a new versioning system was put into place. It works off the following:

Reserved.Major.Minor.Revision.Build

So for 3.2.1.0.0 the major number is 2 and minor number is 1 and revision number is 0. Reserved is used as a base, only
incremented on complete rewrites. The build number is optional and should be 0 on releases.

Major should be incremented when large changes/features are made.

Minor should be incremented when small changes/features are made.

Revision should be incremented when there are no new features and only contains bug fixes for the previous minor.

Build is used for beta releases allowing you to have higher version numbers but force users to update when the real
release comes.

## Need Help/Have Questions?

If you have questions please don't hesitate to [contact us](https://www.atlauncher.com/contact-us/)

## License

This work is licensed under the GNU General Public License v3.0. To view a copy of this license, visit
http://www.gnu.org/licenses/gpl-3.0.txt.

A simple way to keep in terms of the license is by forking this repository and leaving it open source under the same
license. We love free software, seeing people use our code and then not share the code, breaking the license, is
saddening. So please take a look at the license and respect what we're doing.

Also, while we cannot enforce this under the license, you cannot use our CDN/files/assets/modpacks on your own launcher.
Again we cannot enforce this under the license, but needless to say, we'd be very unhappy if you did that and really
would like to leave cease and desist letters as a last resort.

If you have any questions or concerns as to the license or what we consider to be good and bad in your clone/fork,
please use the contact link in the section right above this one.


[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FDev-Osmium%2FATLauncher.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FDev-Osmium%2FATLauncher?ref=badge_large)