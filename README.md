[![Travis](https://img.shields.io/travis/APISENSE/rhino-android.svg)](https://travis-ci.org/APISENSE/rhino-android)
[![Codecov](https://img.shields.io/codecov/c/github/APISENSE/rhino-android.svg)](https://codecov.io/gh/APISENSE/rhino-android)
[![Maven Central](https://img.shields.io/maven-central/v/io.apisense/rhino-android.svg)](http://search.maven.org/#artifactdetails%7Cio.apisense%7Crhino-android%7C1.0%7Cjar)


# Rhino script engine

This project aims to package a minimal Rhino script engine for Android. 

The script engine source code is imported from openjdk implementation, version _7u40-b43_.

## Installation

Add the following repository and dependency to your `build.gradle`:

```
dependencies {
    compile 'io.apisense:rhino-android:1.2.0'
}
```

## Usage

You can now call the Rhino script engine by using the jsr223, i.e.:

```
ScriptEngine engine = new ScriptEngineManager().getEngineByName("rhino");
```

## Configuration

The `ScriptEngine` feature relies on reflection to instanciate the engines. 
This will cause trouble while shrinking your code using Proguard or R8.

To ease the integration of `rhino-android` in your project, you can find a sample project with up-to-date configuration for minification here: https://github.com/aveuiller/RhinoSampleApp
