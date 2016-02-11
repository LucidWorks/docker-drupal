FROM drupal:7.41

MAINTAINER Dmitry Tokarev <dmitry.tokarev@lucidworks.com>


#    ===================================================================
#    The following setup was done on OS X 10.11.2:

#    $ docker-machine start default
#    $ eval "$(docker-machine env default)"
#    $ docker run --name mydrupal -p 8080:80 -d drupal:7.41

#    go to http://192.168.99.100:8080/install.php
#    Choose Standard >> Save and Continue
#    English >> Save and Continue
#    DB type: SQLite
#    DB file: sites/default/files/.ht.sqlite
#    Advanced: default
#    site name: drupaltest
#    site email: dmitry.tokarev@lucidworks.com
#
#    SITE MAINTENANCE ACCOUNT
#    Username: tester
#    email: dmitry.tokarev@lucidworks.com
#    password: Gotester1!
#
#    SERVER SETTINGS
#    Country: USA
#    Time: LA
#
#    UPDATE NOTIFICATIONS
#    Check for updates automatically: OFF
#    Save and continue
#
#    Visit your new site
#    =====================================================================
#    go to http://192.168.99.100:8080/#overlay=admin/modules
#    enable Update manager >> Save configuration
#
#    Install new modules: go to http://192.168.99.100:8080/#overlay=admin/modules/install
#
#    Install from URL: https://ftp.drupal.org/files/projects/ctools-7.x-1.9.tar.gz  >> Install
#
#    Enable newly installed modules:
#    Enable all clickable modules in CHAOS TOOL SUITE
#
#    Install New module: https://ftp.drupal.org/files/projects/libraries-7.x-2.2.tar.gz
#    Enable newly installed modules: Libraries
#
#    Install New module: https://ftp.drupal.org/files/projects/services-7.x-3.13.tar.gz
#    Enable: Services and REST Server
#
#    Click on Configure under Services on http://192.168.99.100:8080/admin/modules page
#    Click on Add:
#        Machine-readable name of the endpoint: rest
#        Server: REST
#        Path to endpoint: rest
#        Debug Mode Enabled: Checked
#        Session authentication: checked
#    Save
#
#    On page http://192.168.99.100:8080/admin/structure/services click on Edit Resources
#    Check all boxes
#    Aliases:
#        comment			    comment
#        file                   file
#        node                   node
#        system                 system
#        taxonomy_term          taxonomy_term
#        taxonomy_vocabulary    taxonomy_vocabulary
#        user                   user
#    Save
#
#
#    On page http://192.168.99.100:8080/admin/structure/services/list/rest/server (SERVER tab)
#    check all boxes
#    Save
#
#    Test if setup was successful: go to http://192.168.99.100:8080/rest
#    ===================================================================
#    Commit changes:
#    $ docker ps -a
#    CONTAINER ID        IMAGE               COMMAND                CREATED             STATUS              PORTS                  NAMES
#    1c38341528dd        drupal:7.41         "apache2-foreground"   2 hours ago         Up About an hour    0.0.0.0:8080->80/tcp   mydrupal
#    $ docker commit 1c38341528dd drupal:drupal7_rest
