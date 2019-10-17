# pd-stream
streaming objects for puredata (Forked from various places)
 right now mp3cast~ but will be more maybe


OSX Build

$ brew install lame && brew install mpg123

$ make

$ chmod 755 pd-osx-deps.sh

$ ./pd-osx-deps.sh


NOTES

after running pd-osx-deps.sh you may have errors depending on how the .dynlib was compiled. Run otool to get some info on .dynlib like so:

macOS
$ otool -hV libmp3lame.0.dylib 

Also to figure out what .dylib is link to a binary:

Linux
$ ldd <binary>

macOS
$ otool -L <binary>
