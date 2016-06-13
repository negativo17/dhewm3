     _ _                             _____
  __| | |__   _____      ___ __ ___ |___ / 
 / _` | '_ \ / _ \ \ /\ / / '_ ` _ \  |_ \
| (_| | | | |  __/\ V  V /| | | | | |___) |
 \__,_|_| |_|\___| \_/\_/ |_| |_| |_|____/

** Doom 3 GPL source modification

For the additional features and fixes introduced by this great modification,
please see the original page at:

 https://github.com/dhewm/dhewm3

======== Game data

It DOES NOT include game data required to run the game, you have to get the data
yourself buying the game.

To launch the engine pointing at your data files you can use the following
command:

 doom3-engine +set fs_basepath "/path/to/game/content" "$@"

A sample nosrc rpm that can be used to build a binary rpm using the DVD data
files is at: http://slaanesh.fedorapeople.org/

To rebuild it, add the required files to your SOURCES directory and remove the
"NoSource" lines in the spec file.

A high resolution icon has been generated from the game assets, to have a look
at how the resulting menu entries look like see:
http://slaanesh.fedorapeople.org/doom3-menus.png

You should end up with something like this:

 $ rpm -qa dhewm3* doom3*
 dhewm3-1.4.1rc1-1.git.89f227b.fc23.x86_64
 doom3-1.3.1.1304-4.fc18.noarch
 doom3-roe-1.3.1.1304-4.fc18.noarch

======== Options defined at compile time

- Uses unbundled Fedora libraries for the following components:
    OpenAL
    Curl
    Ogg Vorbis
    SDL
    zlib
- Uses SDL2 on Fedora and RHEL/CentOS 7+.
- Provides a doom3-engine symlink through the alternatives system to easily
  switch between additional variations.
