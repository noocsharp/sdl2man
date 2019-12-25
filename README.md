### sdl2man

This utility converts SDLWiki pages to manpages. Using the RecentChanges page on the SDLWiki, it can also figure out which wiki pages have been updated, and update the man pages accordingly.

Currently it works well for many pages but not so well for others. I plan to continue to develop this while using it, but pull requests are always welcome.

The script requires the requests library.

    usage: sdl2man [-h] [-p | -f] [-t TIME_INTERVAL] [-g] [-i]

    optional arguments:
      -h, --help            show this help message and exit
      -p, --pull            downloads updated copies of changed pages
      -f, --fresh           removes local copies of pages and redownloads
      -t TIME_INTERVAL, --time-interval TIME_INTERVAL
                            sets time interval on page downloads in seconds (to
                            avoid rate limiting), default is 10
      -g, --generate        generates manpages from local copies

    The generated man pages will be located at $XDG_DATA_HOME/sdl2man/man (usually
    .local/share/sdl2man/man). They can be installed by running the script in the
    sdl2man directory, or by adding the man directory to your MANPATH.
