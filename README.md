> **Maintainer needed**  
> This middleware was ported from Python to Swift for Munki 7 by Greg Neagle. However, Greg does not actually use this middleware and is not particularly motivated to support it. If you or your organization rely on this middleware, please consider taking over the responsibility for maintaining it.

This is a project that builds a CloudFront middleware plugin for Munki 7.

It is a port of Aaron Burchfield's CloudFront-Middleware:
https://github.com/AaronBurchfield/CloudFront-Middleware

Some unit testing is in place to confirm that given the same inputs, the Swift implementation generates the same outputs as the Python implementation. A brief test against a repo hosted on CloudFront was successful (thanks @natewalck and @lashomb).

This plugin requires Munki 7.0.0.5152 or later.

Configuration is the same as the Python plugin, starting with Step 2 [here](https://github.com/AaronBurchfield/CloudFront-Middleware#configure-a-managed-client-to-access-the-cloudfront-munki-repo).

If you use a `munkiaccess.pem` file, the preferred location of this file is `/usr/local/munki/middleware/munkiaccess.pem`, but the path `/usr/local/munki/munkiaccess.pem` (which is used by the Python implementation of this middleware) should work as well.

You may download an Installer package for the current release of the middleware plugin from the [Releases](https://github.com/munki/CloudFrontMiddleware/releases) section.

To build the middleware plugin and an Installer pkg that installs it, `git clone` this project, `cd` into the project directory, and run `./build_pkg.sh`. You will need a recent version of Xcode.
