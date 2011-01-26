A set of scripts that archive content posted to friendfeed feeds.  Stores all the content in an sqlite3 database, so 

Developed and tested on python2.7, should work on python2.6.  I believe most of the python modules it requires are standard/come with a default python installation.  Also needs the simplejson and sqlite3 python modules.

# Functionality currently implemented
 * download all entries from a feed and related media from the entries
 * generate some simple statistics from the downloaded data:

        Statistics for the band-horse-boat-names feed on friendfeed:
              total entries  2613
            deleted entries  0
               oldest entry  2009-07-08T06:27:40Z
          most recent entry  2011-01-25T06:45:38Z
          avg posts per day  5.24
         avg posts per week  31.11
        avg posts per month  137.53
                media files  15
          media type counts    13 image/jpeg
                                2 image/png

# Usage

 * download and create directories named `cache` and `dbs` in the same dir you'll run it from
 * run it as `friendfeed-archive <feedname>`, each feed ends up in its own database file, so if you want to archive a group/room, specifiy the group/room's feedname.
 * put it in cron to run every 15 minutes or so (make sure you cd


# To do (not an exhaustive list)
 * create the directories, make the --cachedir and --dbdir options work


# Planned features
 * generation of a web page with all the content, browsable similar to how it is on the friendfeed website
 * searchable content
 * feed statistics
 * also archive your likes and comments
