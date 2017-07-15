GtkFlow
=======

Here you see libgtkflow, a universal library for drawing flow graphs with
Gtk+ 3.

![GtkFlowMultisink](https://i.imgur.com/4E53t0n.png)

We now have Sinks that can receive data from multiple sources!

![GtkFlowColor](https://i.imgur.com/ZEOFKW6.png)

A more recent screenshot showing off libgtkflow with Gtk > 3.20. It looks
a bit clearer.

![LibGtkFlow](https://i.imgur.com/N10yBKP.png)

This is libgtkflow running inside firefox via broadway ↑

![GtkFlowWindows](https://i.imgur.com/lna1nfB.png)

GtkFlow runs unter that strange M$-operating-system, too ↑

![GtkFlowRes](https://i.imgur.com/RL6Fl3R.png)

The newest stuff in libgtkflow's development ↑
Nodes can be deleted by clicking the X-button in the upper right corner.
Nodes are resizable by drag-n-dropping the lower right corner. The types of the docks can be printed along with their names

![GtkFlowEvopop](http://i.imgur.com/s7qbTPT.png)

This is a screenshot of libgtkflow rendered with the evopop Gtk3 theme ↑

![GtkFlow](https://i.imgur.com/BWcXGkV.png)

This here is the included advanced calculator demo application ↑

Flow graphs are a possibility to let your user model flows of data from, through
and into several stations.

Motivation
----------

I love Flowgraphs in other programs and i want to have them in my favourite
UI-toolkit Gtk. I ran into some programs which implemented similar functionality
but they all didn't feel or even lokk very Gtk-like/GNOMEy.

Possible Usages
---------------

Specific:

  * Writing a UI for [GStreamer](http://gstreamer.org)
  * Writing a UI for [Beehive](https://github.com/muesli/beehive)
  * Replacement for the UI in [Gnuradio](http://gnuradio.org)
  * Matching monitors / inputs / outputs in [Pavucontrol](http://freedesktop.org/software/pulseaudio/pavucontrol/)
  * Writing a UI for [GEGL](http://gegl.org)

Unspecific:

  * Video Compositing (maybe [PiTiVi](http://www.pitivi.org))
  * Visualizing dependencies of objects (e.g. debian packages in apt)

  * … and whatever you can think up.

Stability
-------------

Consider the API unstable for now.
You will encounter bugs.

Building
--------

Make sure you get the following Dependencies:

  * libgtk-3-dev
  * gobject-introspection
  * meson
  * vala
  * (valadoc)

Then do the following:

```
$ git clone https://github.com/grindhold/libgtkflow
$ cd libgtkflow
$ mkdir build
$ cd build
$ meson ..
$ ninja
# sudo ninja install
```

Examples
--------

libgtkflow supports GObject-Introspection which means you can consume it in various
popular languages including but not limited to: Python, Perl, Lua, JS, PHP.
I compiled some examples on how to program against the library in Python in the examples-folder.

Feel free to add examples for your favorite language.

Note: If you installed the library in /usr/local, you have to export the following
environment variables for the examples to work:

```
$ export LD_LIBRARY_PATH=/usr/local/lib/x86_64-linux-gnu
$ export GI_TYPELIB_PATH=/usr/local/lib/x86_64-linux-gnu/girepository-1.0/
```

Please be aware that on other architectures than amd64 you will have to change the
multiarch string ```x86_64-linux-gnu``` to something else that makes sense on your
machine.
