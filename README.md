A set of scripts that archive content posted to friendfeed feeds.  Stores all the content in an sqlite3 database, so everything is self-contained.

Developed and tested on python2.7, should work on python2.6.  I believe most of the python modules it requires are standard/come with a default python installation.  Also needs the simplejson and sqlite3 python modules.

# Functionality currently implemented
 * download all entries from a feed and related media from the entries
 * generate some simple statistics from the downloaded data:

        Statistics for the band-horse-boat-names feed on friendfeed:

              total entries  2986
            deleted entries  0
               oldest entry  2009-07-08T06:27:40Z
          most recent entry  2011-05-31T22:25:23Z

          avg posts per day  4.90
         avg posts per week  29.27
        avg posts per month  129.83

                media files  15
          media type counts    13 image/jpeg
                                2 image/png

# Usage

 * download and create directories named `cache` and `dbs` in the same dir you'll run it from
 * run it as `friendfeed-archive <feedname>`, each feed ends up in its own database file, so if you want to archive a group/room, specifiy the group/room's feedname.
 * put it in cron to run every 15 minutes or so (for now, you'll need to make sure the current directory has the `cache` and `dbs` dirs)


# To do (not an exhaustive list)
 * create the directories, make the --cachedir and --dbdir options work
 * write a web front end that displays the database contents


# Planned features
 * generation of a web page with all the content, browsable similar to how it is on the friendfeed website
 * searchable content
 * feed statistics
 * also archive your likes and comments
