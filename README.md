# MSFTBX Examples
Companion repo for MSFTBX - mass spectrometry data readers library: http://github.com/chhh/msftbx.  
**Provides a complete example java app built with Gradle that prints some information about MS2 scans.**

## Running it
You don't need to have gradle or any libraries installed.
Bootstrapping feature will get everything needed automatically.

### Automatically build and run
```shell
./gradlew run --args "path-to-mzml-or-mzxml-file"
```
This command will build the application jar and start it with your default Java, passing it the values
you specify after `--args`.

### Manually build and run
Alternatively you can tell gradle to build the app and create launch scripts for it (windows and linux)
```shell
./gradlew clean install
```
This command will produce output in `build/install/msftbx-examples`. Run scripts will be in `bin` sub-directory,
and all the jar dependencies will be in `lib` sub-directory.  
You just start the script for your OS from the `bin` directory.

By modifying the `build.gradle` file it's also easy to package the
whole application in a single fat jar file. See [`gradle-shadow`](https://imperceptiblethoughts.com/shadow/) plugin.

### Run from Intellij Idea
You can just import the project into Intellij IDEA and click the green Run triangle icon next to `main()` method of `msftbx.examples.App`.
To import, start IDEA, if you get into its launcher First, click `Open or Import`. if you already have it running with some project open:
`File -> New -> Project from Existing Sources`. Select the `build.gradle` file. IDEA will offer you to open the project in a new window.

If it's your first time using gradle, it might take a while to initially download all dependencies. After the initial import everything
will be very fast.
