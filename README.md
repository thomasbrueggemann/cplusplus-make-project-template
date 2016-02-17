# C++ Make Project Template
A Simple C++ Project Structure following the ideas of http://hiltmon.com/blog/2013/07/03/a-simple-c-plus-plus-project-structure/

## Project Structure

![](http://hiltmon.com/images/simple-cpp-folders.jpg)

For each application, the folders are:

* __bin__: The output executables go here, both for the app and for any tests and spikes.
* __build__: This folder contains all object files, and is removed on a clean.
* __doc__: Any notes, like my assembly notes and configuration files, are here. I decided to create the development and production config files in here instead of in a separate config folder as they “document” the configuration.
* __include__: All project header files. All necessary third-party header files that do not exist under /usr/local/include are also placed here.
* __lib__: Any libs that get compiled by the project, third party or any needed in development. Prior to deployment, third party libraries get moved to /usr/local/lib where they belong, leaving the project clean enough to compile on our Linux deployment servers. I really use this to test different library versions than the standard.
* __spike__: I often write smaller classes or files to test technologies or ideas, and keep them around for future reference. They go here, where they do not dilute the real application’s files, but can still be found later.
* __src__: The application and only the application’s source files.
* __test__: All test code files. You do write tests, no?
