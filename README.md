This is a demo project that builds a CloudFront middleware plugin for Munki 7.

It is a port of Aaron Burchfield's CloudFront-Middleware:
https://github.com/AaronBurchfield/CloudFront-Middleware

Some unit testing is in place to confirm that given the same inputs, the Swift implementation generates the same outputs as the Python implementation. A brief test against a repo hosted on CloudFront was successful (thanks @natewalck and @lashomb).

The middleware plugin must be installed in `/usr/local/munki/middleware/`, and you need Munki 7.0.0.5152 or later to test.

If you use a `munkiaccess.pem` file, the preferred location of this file is `/usr/local/munki/middleware/munkiaccess.pem`, but the path `/usr/local/munki/munkiaccess.pem` (which is used by the Python implementation of this middleware) should work as well.

You can find the installer pkg at https://github.com/munki/CloudFrontMiddleware/releases

If you prefer to build the middleware plugin and an Installer pkg that installs it, cd into this directory and run `./build_pkg.sh`. You will need a recent version of Xcode.
