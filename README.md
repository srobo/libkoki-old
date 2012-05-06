
**libkoki** provides a marker based vision system,
 developed for use in the [Student Robotics](https://www.studentrobotics.org/).


### Build Requirements

In order to build libkoki you'll need to have:

 * A C compiler
 * OpenCV headers
 * YAML headers
 * OpenGL Utility Toolkit

On Ubuntu 11.10 and 11.04, these can be installed using:

~~~~~~~~~~~~~~~~
(sudo) $ apt-get install gcc libcv-dev libhighgui-dev libcvaux-dev libyaml-dev freeglut3-dev
~~~~~~~~~~~~~~~~
### Building and installing

To build and install the libkoki library to the system you must run the
following commands:

~~~~~~~~~~~~~~~~
$ make
$ sudo make install
~~~~~~~~~~~~~~~~

### Examples

libkoki contains a number of examples programs that help demonstrate how
to use the API, as well as some of its capabilities.
The examples can be built by running `make` on their directory, and are
built as part of a default build.

In order to run the examples (without installing libkoki) you should run
the `shell` script in the root of the repository, and then cd into the
examples directory:

~~~~~~~~~~~~~~~~
$ ./shell && cd examples
~~~~~~~~~~~~~~~~

From there you can run any of examples by runnnig them as local programs.
For instance:

~~~~~~~~~~~~~~~~
$ ./realtime_gl
~~~~~~~~~~~~~~~~

Note that some of them expect to be passed an image file as their first
(and only) argument:

~~~~~~~~~~~~~~~~
$ ./marker_info image_from_camera.jpg
~~~~~~~~~~~~~~~~

If get an error that looks a bit like:

~~~~~~~~~~~~~~~~
$ ./examples/realtime_quads
./examples/realtime_quads: error while loading shared libraries: libkoki.so: cannot open shared object file: No such file or directory
~~~~~~~~~~~~~~~~

Then most likely you've forgotten to run `./shell`.
