standalone-war readme

What does it do?
This is a simple gradle build that takes a war and repackages it with an embedded Jetty server.

Preqs
Install gradle 0.8 or later. Internet connection, gradle downloads jetty-embedded on the fly.

Usage
The build takes 2 paramters, inWar and outWar. inWar is required and is the path to the war you'd like to repackage. Specify the params either on commandline with the -P option or in gradle.properties (see gradle.properties.example). If outWar isn't specified the build will default to creating the repackaged war in build/name-standalone.war.

gradle -PinWar=webapp.war
Creates: build/webapp-standalone.war

The standalone can be run with java -jar webapp-standalone.war or put in your favourite servlet container as usual.

Disclaimer
The Jetty starter is in no way heavily tested, use at your own risk.
