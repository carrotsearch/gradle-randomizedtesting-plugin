
# Gradle RandomizedTesting Plugin

Convention defaults and tweaks for Java projects utilizing randomizedtesting libraries.
This plugin contributes the following:

* prints the random seed at the start of each test task,
* disables HTML report generation from tests (slow, not really useful),
* fails the build if no tests have been executed globally,
* adds a "repro line" to the log, if a test task has failed,
* captures test output to plain text files or echoes them to the console in verbose mode,
* adds a global extension ```randomizedtesting```, with ```failOnNoTests``` boolean property and 
  ```testOpts``` containing test options.
* a list of test options and their current overrides can be shown by running ```showOpts``` task.
* contributes multiple ```tests.*``` system/ project properties which can be used to
  override the default test runner options (run ```showOpts``` to see the defaults).

## Usage

You can add it to your top-level build script using the following:

### `plugins` block:

```groovy
plugins {
  id "com.carrotsearch.gradle.randomizedtesting" version "$version"
}
```
