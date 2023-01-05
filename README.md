# remove-old-kernels
Old kernel removal tool for Mageia
Remove old kernels safely and cleanly using urpme.

Once installed it may be left to do it's job without user intervention.

It is run by cron.weekly to retain a minimum number of installed kernels
of each flavour. (Default is three)
This may be adjusted or disabled using simple command line options if desired.

There is also an advanced mode.

It may also be run manually in interactive mode from the desktop menu,
under Tools -> System tools.

Running as normal user from the command line will display the current status
of installed kernels but will not allow removal.

For more information see: 'man remove-old-kernels' or 'man rok' in a terminal.
