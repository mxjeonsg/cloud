## Start

**First** download the Godot 4 engine release for Linux, it's in a .tar.gz file, and its contents are just the executable, uncompress it wherever you want but somewhere reachable, maybe in /opt/Godot if you will, but you can do it in the desktop as well.

**Second** git clone the wattesigma project (you can add --depth=1 to the command line to not download all the commit history bundled, but you can open the GitHub repo page and download everything as a zip, it doesn't matter)

**Third** search for Linux's GDCEF artifacts (the ones I used are Lecrapouille/gdcef, download the last release (it's called "gdcef-artifacts-godot_4-linux_x86_64.tar.gz))

**Fourth** Uncompress the artifacts, copying (or moving) the `cef_artifacts` folder inside the wattesigma folder at the root of the folder specifically.

**Fifth** Open Godot, and import the wattesigma folder.

**Sixth** Go to Project/Export... and try to export it for Linux/X11, it'll fail at first because it misses the export templates, just do it, the pop up has the download button, it'll download the whole 1GB thing and install it by itself, just reach a coffee or touch some grass.

**Seventh** Go to Project/Export... again, and export it to Linux/X11, it will finally export, dropping a file named around "CEFgd.x86_64" in the folder's root, run it and there you go.

## Considerations
- You can't pull out the binary outside the project folder, it depends on everything there, assets, libraries and the artifacts, just move the entire folder wherever you want, but the whole project folder, otherwise it won't run adequately.
- When you run it, it might cry about Vulkan incompatibility if your Linux kernel hates your computer, just dismiss it, it will run nonetheless, it defaults to opengl3 I think, but it works.
