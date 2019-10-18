# pd-stream
streaming objects for puredata (Forked from various places)
 right now mp3cast~ works but the others crash on me... go figure


OSX Build

$ brew install lame && brew install mpg123

$ make

$ chmod 755 pd-osx-deps.sh

$ ./pd-osx-deps.sh


NOTES

mp3amp~ complaining of "Symbol not found: _ExitMP3", "Symbol not found: _freqs", etc. I am assuming here that mpglib must be installed but with homebrew it is not available... hmmmm


after running pd-osx-deps.sh you may have errors depending on how the .dynlib was compiled. Run otool to get some info on .dynlib like so:

macOS
$ otool -hV libmp3lame.0.dylib 

Also to figure out what .dylib is link to a binary:

Linux
$ ldd <binary>

macOS
$ otool -L <binary>
