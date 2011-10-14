!SLIDE
# Drush Make
The theory, the practice, the future

!SLIDE
# About me
* Jonathan Hedstrom
* [@jhedstro](http://twitter.com/jhedstro)
* [jhedstrom](http://drupal.org/user/208732)

!SLIDE
# Drush Make
Some quick examples

!SLIDE subsection
Core + Views
    @@@ conf
    ; Core, latest version
	projects[] = drupal
    
    ; Views, latest version
    projects[] = views

!SLIDE subsection
Specific versions
    @@@ conf
    projects[views][version] = 3.0

!SLIDE
# Why

!SLIDE
Site manifest

!SLIDE
Easy for developers to quickly get up to speed on a project

!SLIDE
Encourages contributing back to the community

(Which encourages well thought out patches instead of hacks)

!SLIDE
# Advanced usage

!SLIDE subsection small
Patches
    @@@ conf
    projects[spaces][subdir] = "contrib"
    projects[spaces][version] = "3.1"
    ; Patch spaces: http://drupal.org/node/976324#comment-4354134
    projects[spaces][patch][] = "http://drupal.org/files/issues/spaces.976324-08.patch"
    ; Patch spaces: http://drupal.org/node/1232804#comment-4794526
    projects[spaces][patch][] = "http://drupal.org/files/issues/1232804-spaces_og_group_node_403.patch"

!SLIDE subsection small
Customizing Distributions
    @@@ conf
	; OpenAtrium
    projects[openatrium][type] = "profile"
    projects[openatrium][download][type] = "git"
    projects[openatrium][download][tag] = "6.x-1.0"
    
    ; Additional modules
    projects[editablefields][subdir] = "contrib"
    projects[editablefields][version] = "2.0"

!SLIDE subsection small
Atrium with Pressflow
    @@@ conf
	; Pressflow
    projects[pressflow][type] = "core"
    projects[pressflow][download][type] = "file"
    projects[pressflow][download][url] = "http://launchpad.net/pressflow/6.x/6.22.104/+download/pressflow-6.22.104.tar.gz"

	; OpenAtrium
    projects[openatrium][type] = "profile"
    projects[openatrium][download][type] = "git"
    projects[openatrium][download][tag] = "6.x-1.0"

!SLIDE subsection small
# Advanced usage
    @@@ bash
    # working copy
	drush make --working-copy foo.make

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
