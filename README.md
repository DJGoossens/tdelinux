# tdelinux
The TDE editor compiled for Linux

The TDE editor is small, flexible and powerful. The main website (http://adoxa.altervista.org/tde/) provides binaries for DOS and Windows. This repo just provides Linux files, including a binary compiled on 64-bit Debian and a man page. There is no installer -- you just unpack the archive, put a link to the TDE binary in your ~/bin directory, add the man page to your local man tree, and add the TDEHOME environment variable to your login script.

TDEHOME points to the directory where the TDE binary lives (the binary, not the link), and which also has the config directory as a subdirectory. The config directory contains syntax highlighting, configuration and keyboard mapping files that allow you to customise almost everything about the editor, from colours to keybindings. Read about it in the excellent TDE docs that come with it.

That's one of the interesting things about TDE -- you can customise it so much it's almost like writing your own editor program.

Blog post on the topic is at https://darrengoossens.wordpress.com/2025/06/10/the-tde-editor-on-64-bit-linux-in-2023-including-a-man-page/.

Other, much more useful page is: https://www.pement.org/tde.htm

In brief, you can compile it yourself via:

    $ wget http://adoxa.altervista.org/tde/tde-5.1v.tar.gz
    $ tar xvzf tde-5.1v.tar.gz
    $ cd tde-5.1v/
    $ wget http://adoxa.altervista.org/tde/linux64.patch
    $ patch -p1 < linux64.patch
    $ make

And then install manually. (Take the man page from the archive.)

darren.goossens@gmail.com

11 March 2026
