!SLIDE
# Drush Make
## The theory, the practice, the future

!SLIDE
# About me
* Jonathan Hedstrom
* [@jhedstro](http://twitter.com/jhedstro)
* [jhedstrom](http://drupal.org/user/208732)

!SLIDE subsection
# Basic examples
    @@@ conf
    ; Core + Views
	projects[] = drupal
    projects[] = views

!SLIDE subsection
# Basic examples
    @@@ conf
    ; Specific versions
    projects[views][version] = 3.0

!SLIDE subsection
# Basic examples
    @@@ conf
    ; External libraries
    TODO

!SLIDE bullets incremental
# Why
 * Site manifest
 * Easy for developers to quickly get up to speed on a project
 * Encourages contributing back to the community
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
