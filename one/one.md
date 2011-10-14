!SLIDE
# Drush Make
## The theory, the practice, the future

!SLIDE
# About me
* Jonathan Hedstrom
* [@jhedstro](http://twitter.com/jhedstro)
* [jhedstrom](http://drupal.org/user/208732)

!SLIDE
# Drush Make
Some quick examples

!SLIDE subsection
# Basic examples
    @@@ conf
    ; Core, latest version
	projects[] = drupal
    
    ; Views, latest version
    projects[] = views

!SLIDE subsection
# Basic examples
    @@@ conf
    ; Specific versions
    projects[views][version] = 3.0

!SLIDE
# Why
Site manifest

!SLIDE
# WHY
Easy for developers to quickly get up to speed on a project

!SLIDE
# WHY
Encourages contributing back to the community

(Which encourages well thought out patches instead of hacks)

!SLIDE
# Advanced usage

!SLIDE subsection
# Advanced usage
    @@@ conf
    ; Patches
    TODO

!SLIDE subsection
# Advanced usage
    @@@ conf
	; Customizing distributions
	TODO

!SLIDE subsection
# Advanced usage
    @@@ bash
    # working copy
    TODO

!SLIDE subsection small
# Advanced usage
    @@@ conf
    ; External libraries
    libraries[SolrPHPClient][download][type] = "svn"
    libraries[SolrPHPClient][download][url] = "http://solr-php-client.googlecode.com/svn/trunk/"
    libraries[SolrPHPClient][download][revision] = "22"
    libraries[SolrPHPClient][destination] = "modules/apachesolr/"
    libraries[SolrPHPClient][directory_name] = "SolrPhpClient"

    ; jQuery UI
    projects[jquery_ui][version] = "1.4"
    libraries[jquery_ui][download][type] = "get"
    libraries[jquery_ui][download][url] = "http://jquery-ui.googlecode.com/files/jquery.ui-1.6.zip"
    libraries[jquery_ui][directory_name] = "jquery.ui"
    libraries[jquery_ui][destination] = "modules/jquery_ui"

!SLIDE
# Sample development workflow
TODO

!SLIDE subsection small bullets incremental
# Things that could be better
* Deployment support
* <s>Acquia</s> (no)
* <s>Pantheon</s> (no)
* Aegir (yes)
* Solution?
* Drush Deploy strategy.

!SLIDE subsection bullets incremental
# Things that could be better
* `drush pm-update`
* External dependencies

!SLIDE bullets incremental
# The future of make
* `drush pm-update` needs an option to update the .make file
* Caching of downloads (currently, use squid)
* Drush 5 does this
* Better support

!SLIDE bullets incremental
# The future of make
* which means ...
* ### Put make in drush core
* http://drupal.org/node/1310130

!SLIDE bullets incremental
# Thank you
* node #1310130
* Presentation made with Showoff
* ###Questions?
