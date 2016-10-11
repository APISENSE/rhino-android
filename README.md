# Rhino script engine

This project aims to package a minimal Rhino script engine for Android. 

The script engine source code is imported from openjdk implementation, version _7u40-b43_.

## Installation

Add the following repository and dependency to your `build.gradle`:

```
dependencies {
    compile 'io.apisense:rhino-android:1.0'
}
```

## Usage

You can now call the Rhino script engine by using the jsr223, i.e.:

```
ScriptEngine engine = new ScriptEngineManager().getEngineByName("rhino");
```
