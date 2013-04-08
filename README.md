jetty-buildpack
===========================

Buildpack plugin for Jetty.

[![Build Status](https://travis-ci.org/jmcc0nn3ll/jetty-buildpack.png)](https://travis-ci.org/jmcc0nn3ll/jetty-buildpack)

> Note:
> This buildpack was created with the V2 cloudfoundry mechanism and on an alpha release of CFM (micro) at that.  Take
> this with a grain of salt and be prepared for required changes should significant changes end up being flushed out
> before that goes live.

This buildpack is quite simple to use.  It is currently hard coded to a specific Jetty version of 9.0.1.v20130408 and to
change that the apparent approach is to simply fork this buildpack and tweak that directly.  To do this simply fork it 
in GitHub and tweak the JETTY_VERSION string in the jetty_web.rb file.

If you have modifications to make to make the to Jetty server that will be running, like perhaps configuring additional
static contexts, setting up a proxy servlet, adding items to the jetty.home/lib/ext directory, you can either adapt
the ruby scripting or place them under the appropriate location in the resources directory of this buildpack and they 
will be copied into the correct location.

The new CloudFoundry buildpacks seem to be very simple to use and straight forward to setup and customize.  However
*customize* seems to be a really key component so I am unsure how relevant this buildpack will be outside of serving as
root fork for customized jetty buildpack, or just a simple example of how to do one of your own for CloudFoundry.

Feel free to submit feedback via normal github channels and I'll accept pull requests on this should they come.  

For the being I'll leave this buildpack under my personal github account and should there be interest expressed I am 
more then happy to push it over to https://github.com/jetty-project down the road.
