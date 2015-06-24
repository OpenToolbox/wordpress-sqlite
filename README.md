# WordPress Sqlite

## Required

A simple unix shell
         
    mkdir mywordpress
    cd mywordpress

or

A hosted PHP Workspace with cloud9 (https://c9.io/) 

    rm -rf *


### Install the latest WordPress version

    wget https://wordpress.org/latest.zip 
    
    unzip latest.zip ; rm -f latest.zip
    
    mv wordpress/* . ; rm -rf wordpress
    
    mv ./wp-config-sample.php ./wp-config.php


### Install automatic-domain-changer plugin

    wget https://downloads.wordpress.org/plugin/automatic-domain-changer.zip 
    
    unzip automatic-domain-changer.zip -d ./wp-content/plugins/ ; rm -f automatic-domain-changer.zip
    
    echo '/** Sets up Automatic Domain Change. **/ include_once( ABSPATH . "wp-admin/includes/plugin.php" ); if (!is_plugin_active($plugin = ABSPATH . "wp-content/plugins/automatic-domain-changer/auto-domain-change.php")) activate_plugin($plugin);' >> ./wp-config.php


### Install sqlite-integration plugin

    wget http://downloads.wordpress.org/plugin/sqlite-integration.zip
    
    unzip sqlite-integration.zip -d ./wp-content/plugins/ ; rm -f sqlite-integration.zip
    
    cp ./wp-content/plugins/sqlite-integration/db.php ./wp-content/db.php



### Sources

- http://dogwood.skr.jp/wordpress/sqlite-integration/
- https://memberfind.me/automatically-activating-a-wordpress-plugin-on-install/
