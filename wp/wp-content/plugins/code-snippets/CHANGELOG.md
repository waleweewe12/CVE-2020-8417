# Changelog

## 2.13.3 (13 Mar 2019)
* Added: Hover effect to activation switches.
* Added: Additional save buttons above snippet editor.
* Added: List save keyboard shortcuts to the help tooltip.
* Added: Change "no items found" message when search filters match nothing.
* Fixed: Calling deprecated code in database upgrade process.
* Fixed: Include snippet priority in export files.
* Fixed: Use Unix newlines in code export file.
* Updated CodeMirror to version 5.44.0.
* Fixed: Correctly register snippet tables with WordPress to prevent database repair errors [[#](https://wordpress.org/support/topic/database-corrupted-4/)]
* Fixed: CodeMirror indentation settings being applied incorrectly 

## 2.13.2 (25 Jan 2019)
* Removed potentially problematic cursor position saving feature

## 2.13.1 (22 Jan 2019)
* Added: Add menu buttons to settings page for compact menu
* Updated: French translation updated thanks to momo-fr
* Fixed: Split code editor and tag editor scripts into their own files to prevent dependency errors
* Fixed: Handling of single-use shared network snippets
* Fixed: Minor translation template issues
* Added: Help tooltop to snippet editor for keyboard shortcuts, thanks to Michael DeWitt
* Improved: Added button for executing single-use snippets to snippets table
* Added: Sample snippet for ordering snippets table by name by default
* Updated CodeMirror to version 5.43.0

## 2.13.0 (17 Dec 2018)
* Added: Search/replace functionality to the snippet editor. [See here for a list of keyboard shortcuts.](https://codemirror.net/demo/search.html) [[#](https://wordpress.org/support/topic/feature-request-codemirror-search-and-replace/)]
* Updated CodeMirror to version 5.42.0
* Added: Option to make admin menu more compact
* Fixed: Problem clearing recently active snippet list
* Improved: Integration between plugin and the CodeMirror library, to prevent collisions
* Improved: Added additional styles to editor settings preview
* Added: PHP linter to code editor
* Improved: Use external scripts instead of inline scripts
* Fixed: Missing functionality for 'Auto Close Brackets' and 'Highlight Selection Matches' settings

## 2.12.1 (15 Nov 2018)
* Improved: CodeMirror updated to version 5.41.0
* Improved: Attempt to create database columns that might be missing after a table upgrade
* Improved: Streamlined upgrade process
* Fixed: Interface layout on sites using right-to-left languages
* Improved: Made search box appear at top of page on mobile [[#](https://wordpress.org/support/topic/small-modification-for-mobile-ux/)]
* Updated screenshots

## 2.12.0 (23 Sep 2018)
* Removed option for including network-wide snippets in subsite lists on multisite
* Fixed: Prevented hidden columns setting from reverting to default
* Improved: Updated import page to improve usability
* Improved: Added Import button next to page title on manage page
* Improved: Added coloured banner indicating whether a snippet is active when editing
* Update CodeMirror to 5.40.0

## 2.11.0 (24 Jul 2018)
* Added: Ability to assign a priority to snippets, to determine the order in which they are executed
* Improvement: The editor cursor position will be preserved when saving a snippet
* Added: Pressing Ctrl/Cmd + S while writing a snippet will save it
* Added: Shadow opening PHP tag above the code editor
* Improved: Updated the message shown when there are no snippets
* Added: Install sample snippets when the plugin is installed
* Improved: Show all available tags when selecting the tag field
* Added: Filter hook for controlling the default list table view
* Added: Action for cloning snippets

## 2.10.2 (21 Jul 2018)
* Added: Button to reset settings to their default values
* Improved: Made uninstall cleanup optional through a plugin setting
* Fixed: Applied formatting filters to snippet descriptions in the table
* Improved: Ordered tags by name in the filter dropdown menu
* Fixed: Incorrectly translated strings
* Added: Belarusian translation by Hrank.com
* Improved: Enabled sorting snippets table by tags
* Updated CodeMirror to version 5.39.0

## 2.10.1 (10 Feb 2018)
* Fixed: Prevent errors when trying to export no snippets
* Fixed: Use wp_json_encode() to encode export data
* Fixed: Check both the file extension and MIME type of uploaded import files

## 2.10.0 (18 Jan 2018)
* Improved: Added support for importing from multiple export files at once
* Improved: Unbold the titles of inactive snippets for greater visual distinction
* Added: New scope for single-use snippets
* Improved: Don't show network snippets on subsites by default, and only to super admins
* Improved: Export snippets to JSON instead of XML
* Improved: More options for importing duplicate snippets
* Improved: Use strings for representing scopes internally instead of numbers
* Added: Allowed plugin settings to be unified on multisite through Network Settings option
* Fixed: Issue with incorrectly treating network snippets as site-wide for code validation
* Improved: Rename 'Export to PHP' to 'Download', and add button to edit snippet page

## 2.9.6 (14 Jan 2018)
* Added Brazilian Portuguese translation by [Bruno Borges](http://brunoborges.info)
* Fixed: Use standard WordPress capabilities instead of custom capabilities to prevent lockouts
* Fixed: Multisite issue with retrieving active shared snippets from the wrong table causing duplicate snippet execution
* Moved scope and other settings on single snippet page to below code area

## 2.9.5 (13 Jan 2018)
* Fixed: Undefined function error when accessing the database on multisite
* Fixed: Ensured all admin headings are hierarchical for accessibility
* Made the "Activate By Default" setting enabled by default for new installs
* Updated CodeMirror to version 5.33

## 2.9.4 (19 Sep 2017)
* Fixed: Prevented PHP error from occurring when saving a snippet
* Minor improvements to database creation function

## 2.9.3 (11 Sep 2017)
* Fixed: Prevent snippets from being executed twice when saving due to invalid ID being passed to allow_execute_snippet filter
* Fixed: Re-enabled output suppression when executing snippets

## 2.9.2 (8 Sep 2017)
* Fixed: Do not attempt to combine queries for fetching local and multisite snippets

## 2.9.1 (7 Sep 2017)
* Fixed: Prevent illegal mix of collations errors when fetching snippets from database tables with different collations [[#](https://wordpress.org/support/topic/issue-on-multisite-with-wpml/)]

## 2.9.0 (6 Sep 2017)
* Fixed: Prevented invalid properties from being set when saving a snippet
* Fixed: Use the correct protocol when saving a snippet
* Improved: Moved code to disable snippet execution into a filter hook
* Fixed: Active shared snippets not being updated correctly
* Improved: execute_active_snippets() function updated with improved efficiency
* Improved: Renamed Snippet class to avoid name collisions with other plugins
* Improved: Don't hide output when executing a snippet

## 2.8.7 (18 May 2017)
* Added French (Canada) translation by Domonic Desbiens
* Added fixes for Indonesian translation by @zmni

## 2.8.6 (14 May 2017)
* Ensured that get_snippets() function retrieves snippets with the correct 'network' setting. Fixes snippet edit links in network admin.
* Fixed snippet description field alias not mapping correctly, causing snippet descriptions to not be displayed in the table or when editing a snippet

## 2.8.5 (13 May 2017)
* Ensured HTML in snippet titles is escaped in snippets table
* Added Indonesian translation by Jordan Silaen from ChameleonJohn.com 
* Disallowed undefined fields to be set on the Snippets class
* Prevented shared network snippets from being included twice in snippets table on multisite
* Added setting to hide network snippets on subsites

## 2.8.4 (29 April 2017)
* Fixed all snippets being treated as network snippets on non-multisite sites

## 2.8.3 (29 April 2017)
* Updated CodeMirror to version 5.25.0
* Show network active snippets as read-only on multisite subsites
* Added more compete output escaping to prevent XSS errors

## 2.8.2 (27 Feb 2017)
* Fix bug introduced in 2.8.1 that broke code verification functionality by executing code twice

## 2.8.1 (25 Feb 2017)
* Updated German translation
* Fixed admin menu items not translating
* Removed possible conflict between Debug Bar Console plugin (#52)
* Corrected editor alignment on RTL sites ([#](https://wordpress.org/support/topic/suggestion-css-fix-for-rtl-sites/))
* Fixed bulk actions running when Filter button is clicked ([#](https://wordpress.org/support/topic/bug-with-filtering-action-buttons/))
* Updated CodeMirror to version 5.24.0

## 2.8.0 (14 Dec 2016)
* Fixed Italian translation errors. Props to @arsenalemusica
* Renamed 'Manage' admin menu label to 'All Snippets' to keep in line with other admin menu labels
* Renamed placeholder on snippet name field to 'Enter title here'
* Removed CodeMirror search functionality
* Moved 'Edit Snippet' admin menu above 'Add New' menu
* Made pressing Ctrl-Enter in the code editor save the snippet
* Updated CodeMirror to version 5.21.0

## 2.7.3 (24 Oct 2016)
* Updated CodeMirror to version 5.10.0
* Fixed a few strings not being translated

## 2.7.2 (1 Oct 2016)
* Updated German translation by [Mario Siegmann](http://web-alltag.de)

## 2.7.1 (30 Sep 2016)
* Added Dutch translation by Sander Spies
* Ensured that the editor theme setting is properly validated. Thanks to [Netsparker](https://www.netsparker.com) for reporting.
* Ensured that snippet tags are properly escaped. Thanks to [Netsparker](https://www.netsparker.com) for reporting.
* Updated CodeMirror to version 5.19.0

## 2.7.0 (23 July 2016)
* Fixed plugin translations being loaded
* Increase default snippets per page so that all are usually shown
* Fixed description field not being imported
* Updated German translation by [Mario Siegmann](http://web-alltag.de)
* Fixed issue with CodeMirror rubyblue theme [[#](https://wordpress.org/support/topic/a-problem-with-the-cursor-color-and-the-fix-that-worked-for-me)]
* Added query var to disable snippet execution. To use, add `?snippets-safe-mode=true` to the URL
* Fixed snippet fields not importing
* Updated CodeMirror to version 5.17.0
* Fixed a minor XSS vulnerability discovered by Burak Kelebek [[#](https://wordpress.org/support/topic/security-vulnerability-20)]

## 2.6.1 (10 Feb 2016)
* Updated German translation by [Mario Siegmann](http://web-alltag.de)
* Fixed error catching not working correctly
* Updated error catching to work with snippets including functions and classes
* Fixed editor autoresizing

## 2.6.0 (31 Dec 2015)
* Reconfigured plugin to use classloader and converted a lot of functional code into OOP code
* Updated CodeMirror to version 5.10.0
* Added `[code_snippets]` shortcode for embedding snippet code in a post
* Fixed broken snippet search feature [[#](https://wordpress.org/support/topic/search-is-not-working-6)]
* Added front-end syntax highlighting for shortcode using [PrismJS](http://prismjs.com)

## 2.5.1 (11 Oct 2016)
* Fixed: Ensure errors are fatal before catching them during error checking
* Fixed: Escape the snippet name on the edit page to ensure it displays correctly
* Fixed: Exclude snippets with named functions from error checking so they do not run twice

## 2.5.0 (8 Oct 2015)
* Added: Detect parse and fatal errors in code when saving a snippet, and display a user-friendly message
* Fixed: Updated access of some methods in Code_Snippets_List_Table class to match updated WP_List_Table class

## 2.4.2 (27 Sep 2015)
* Added query variable to activate safe mode
* Fixed settings not saving
* Fixed snippet descriptions not displaying on manage menu
* Added settings to disable description and tag editors
* Fixed: Load CodeMirror after plugin styles to fix error with Zenburn theme
* Fixed: Hide snippet scope icons when the scope selector is disabled
* Fixed description heading on edt snippet menu being hidden when visual editor disabled
* Updated editor preview updating code to use vanilla JavaScript instead of jQuery
* Fixed: Deactivate a shared network snippet on all subsites when it looses its sharing status

## 2.4.1 (17 Sep 2015)
* Fixed CodeMirror themes not being detected on settings page [[#](https://wordpress.org/support/topic/updated-to-240-now-i-cant-switch-theme)]

## 2.4.0 (17 Sep 2015)
* Added ability to share network snippets to individual sites on WordPress multisite
* Improved code directory and class structure
* Remove legacy code for pre-3.6 compatibility
* Improved code for printing admin messages
* Updated German translation (Joerg Knoerchen)
* Added `code_snippets/after_execute_snippet` filter
* Added class for individual snippets
* Updated `get_snippets()` function to retrieve individual snippets
* Removed scope statuses and added fixed tags to indicate scope
* Changed admin page headers to use `<h1>` tags instead of `<h2>` tags
* Updated CodeMirror to version 5.6
* Removed snippet settings page from network admin

## 2.3.0 (20 May 2015)
* Removed nested functions
* Added icons for admin and front-end snippets to manage table
* Improved settings retrieval by caching settings
* Updated Russian translation by [Alexey Chumakov](http://chumakov.ru/)
* Added filter switch to prevent a snippet from executing ([#25](https://github.com/sheabunge/code-snippets/issues/25))
* Fixed errors in string translation
* Fixed bug in import process ([#32](https://github.com/sheabunge/code-snippets/issues/32))

## 2.2.3 (13 May 2015)
* Fixed broken call to `export_snippet()` function
* Added support for importing and exporting snippet scope
* Fixed duplicate primary key database error
* Improved database table structure

## 2.2.2 (11 May 2015)
* Polyfilled array_replace_recursive() function for PHP 5.2
* Updated references to old plugin site
* Resolved JavaScript error on edit snippet pages
* Made minor updates to French translation file
* Added statuses for snippet scopes on manage snippets table

## 2.2.1 (10 May 2015)
* Fixed the default values of new setting not being applied
* Fixed missing background of tags input

## 2.2.0 (10 May 2015)
* Introduced CodeSniffer testing on code
* Fixed description heading disappearing when media buttons enabled
* Added snippet scope selector
* Minified all CSS and JS in plugin
* Made CodeMirror theme names more readable
* Fixed bug causing translations to not be loaded

## 2.1.0 (09 May 2015)
* Added additional setting descriptions
* Added settings for code and description editor height
* Updated CodeMirror to version 5.2
* Fixed not escaping the request URL when using query arg functions
* Improved efficiency of settings component

## 2.0.3 (17 Mar 2015)
* Updated German translation by [Joerg Knoerchen](http://www.sensorgrafie.de/)

## 2.0.2 (05 Mar 2015)
* Fix error in table creation code
* Remove settings database option when plugin is uninstalled

## 2.0.1 (25 Feb 2015)
* Fixed table creation code not running on upgrade
* Fixed snippets per page option not saving

## 2.0 (24 Feb 2015)

### Highlights
* Better import/export functionality
* New settings page with code editor settings
* Code rewritten for cleaner and more efficient code
* Lots of new translations

### Added
* Added link to Code Snippets importer under Snippets admin menu
* Added settings component and admin page
* Added support for different CodeMirror themes
* Integrated tags component into main plugin. Current users of the Code Snippets Tags plugin can safely uninstall it.
* Added Auto Close Brackets CodeMirror addon (props to TronicLabs)
* Added Serbo-Croatian translation by Borisa Djuraskovic from [Web Hosting Hub](http://www.webhostinghub.com)
* Added Highlight Selection Matches CodeMirror addon (props to TronicLabs)
* Added Chinese translation thanks to Jincheng Shan
* Added Russian translation by Alexander Samsonov
* Added Slovak translation by [Ján Fajčák] from [WordPress Slovakia](http://wp.sk)
* Added setting to always save and activate snippets by default

### Changed
* Added braces to single-line conditionals in line with [new coding standards](https://make.wordpress.org/core/2013/11/13/proposed-coding-standards-change-always-require-braces/)
* Split up large classes into separate functions
* Improved plugin file structure
* Replaced uninstall hook with single file method
* Updated CodeMirror library to version 5.0
* Rewritten import/export functionality to use DOMDocument
* Merged Code_Snippets_Export_PHP class into Code_Snippets_Export class

### Deprecated
* Removed old admin style support
* Removed backwards-compatible support

### Fixed
* Fixed incompatibility errors with PHP 5.2
* Fixed empty MO translation files
* Removed duplicate MySQL primary key indexing

## 1.9.1.1 (3 Jan 2014)
* Add capability check to site snippets importer

## 1.9.1 (2 Jan 2014)
* Use an icon font for menu icon instead of embedded SVG
* Use Sass (libsass) instead of Compass
* Unminify CodeMirror scripts
* Fixes for the WP 3.8 interface
* Fix 'enable snippets menu for site admins' multisite setting

## 1.9 (11 Nov 2013)
* Add and remove network capabilities as super admins are added and removed
* Updated MP6 icon implementation
* Replaced buggy trim `<?php` and `?>` functionality with a much more reliable regex method ([#](http://wordpress.org/support/topic/character-gets-cut))
* Added French translation thanks to translator [oWEB](http://office-web.net)
* Fixed snippet failing to save when code contains `%` character, props to [nikan06](http://wordpress.org/support/profile/nikan06) ([#](http://wordpress.org/support/topic/percent-sign-bug))
* Added 'Save & Deactivate' button to the edit snippet page ([#](http://wordpress.org/support/topic/deactivate-button-in-edit-snippet-page))
* Removed edit and install capabilities (now only uses the manage capability)
* Fixed HTML breaking in export files ([#](http://wordpress.org/support/topic/import-problem-7))
* Make the title of each snippet on the manage page a clickable link to edit the snippet ([#](http://wordpress.org/support/topic/deactivate-button-in-edit-snippet-page?replies=9#post-4682757))
* Added nonce to edit snippet page
* Hide row actions on manage snippet page by default
* Removed screenshots from plugin
* Improved CodeMirror implementation
* Added a fallback MP6 icon
* Use the proper WordPress database APIs all of the time
* Rewritten export functionality
* Fixed incorrect export filename
* Updated CodeMirror to version 3.19
* Removed CodeMirror bundled with plugin
* Updated WordPress.org plugin banner
* Fixed CodeMirror incompatibility with the WP Editor plugin
* Fixed CodeMirror incompatibility with the Debug Bar Console plugin

## 1.8.1.1 (18 Aug 2013)

## 1.8.1 (29 July 2013)
* Compiled all CodeMirror scripts into a single file
* Use Sass + Compass for CSS
* Use Grunt for build automation
* Minify CSS
* Fixed code typo that was breaking export files
* Updated CodeMirror to 3.15

## 1.8 (9 July 2013)
* Allow no snippet name or code to be set
* Prevented an error on fresh multisite installations
* Refactored code to use best practices
* Improved database table creation method: on a single-site install, the snippets table will always be created. On a multisite install, the network snippets table will always be created; the site-specific table will always be created for the main site; for sub-sites the snippets table will only be created on a visit to a snippets admin page.
* Updated to CodeMirror 3.14
* Changes to filter and action hook API
* Added error message handling for import snippets page
* Don't encode HTML entities in database

## 1.7.1.2 (3 May 2013)
* Correct path to admin menu icon. Fixes [#8](https://github.com/sheabunge/code-snippets/issues/8)

## 1.7.1.1 (29 April 2013)
* Fixed a bug with custom capabilities and admin menus

## 1.7.1 (22 April 2013)
* Fix a bug with snippet being set as deactivated when saved
* Updated PHP Documentation completely. [[View online](http://bungeshea.github.io/code-snippets/api)]
* Only load admin functions when viewing dashboard
* Added German translation thanks to [David Decker](http://deckerweb.de)
* Allow or deny site administrators access to snippet admin menus. Set your preference in the **Enable Administration Menus** setting under the *Settings > Network Settings* network admin menu.
* Improve database table creation and upgrade process
* Optimized to use less database queries

## 1.7 (26 Mar 2013)
* Improved plugin API
* Fixed a bug with saving snippets per page option ([#](http://wordpress.org/support/topic/plugin-code-snippets-snippets-per-page-does-not-work#post-3710991))
* Updated CodeMirror to version 3.11
* Allow plugin to be activated on individual sites on multisite ([#](http://wordpress.org/support/topic/dont-work-at-multisite))
* Slimmed down the description visual editor
* Added icon for the new MP6 admin UI ([#](http://wordpress.org/support/topic/icon-disappears-with-mp6))
* Strip PHP tags from the beginning and end of a snippet on save ([#](http://wordpress.org/support/topic/php-tags))
* Changed to [MIT license](http://opensource.org/licenses/mit-license.php)
* Removed HTML, CSS and JavaScript CodeMirror modes that were messing things up
* Change label in admin menu when editing a snippet
* Improved admin styling
* Made everything leaner, faster, and better

## 1.6.1 (29 Dec 2012)
* Fixed a bug with permissions not being applied on install ([#](http://wordpress.org/support/topic/permissions-problem-after-install))
* Fixed a bug in the uninstall method ([#](http://wordpress.org/support/topic/bug-in-delete-script))

## 1.6 (22 Dec 2012)
* Updated code editor to use CodeMirror 3
* Improved compatibility with Clean Options plugin
* Code improvements and optimization
* Changed namespace from `cs` to `code_snippets`
* Move css and js under assets
* Organized CodeMirror scripts
* Improved updating process
* Current line of code editor is now highlighted
* Highlight matches of selected text in code editor
* Only create snippet tables when needed
* Store multisite only options in site options table
* Fixed compatibility bugs with WordPress 3.5

## 1.5 (18 Sep 2012)
* Updated CodeMirror to version 2.33
* Updated the 'Manage Snippets' page to use the WP_List_Table class
	* Added 'Screen Options' tab to 'Manage Snippets' page
	* Added search capability to 'Manage Snippets' page
	* Added views to easily filter activated, deactivated and recently activated snippets
	* Added ID column to 'Manage Snippets' page
	* Added sortable name and ID column on 'Manage Snippets' page ([#](http://wordpress.org/support/topic/plugin-code-snippets-suggestion-sort-by-snippet-name))
* Added custom capabilities
* Improved API
* Added 'Export to PHP' feature ([#](http://wordpress.org/support/topic/plugin-code-snippets-suggestion-bulk-export-to-php))
* Lengthened snippet name field to 64 characters ([#](http://wordpress.org/support/topic/plugin-code-snippets-snippet-title-limited-to-36-characters))
* Added i18n

## 1.4 (20 Aug 2012)
* Added interface to Network Dashboard
* Updated uninstall to support multisite
* Replaced EditArea with [CodeMirror](http://codemirror.net)
* Small improvements

## 1.3.2 (17 Aug 2012)
* Fixed a bug with version 1.3.1

## 1.3.1 (17 Aug 2012)
* Changed plugin website URI
* Cleaned up some code

## 1.3 (1 Aug 2012)
* Added export option to 'Manage Snippets' page
* Added 'Import Snippets' page

## 1.2 (29 July 2012)
* Minor improvements
* Added code highlighting
* Removed 'Uninstall Plugin' page
* Data will now be cleaned up when plugin is deleted through WordPress admin

## 1.1 (24 June 2012)
* Fixed a permissions bug with `DISALLOW_FILE_EDIT` being set to true ([#](http://wordpress.org/support/topic/plugin-code-snippets-cant-add-new))
* Fixed a bug with the page title reading 'Add New Snippet' on the 'Edit Snippets' page
* Fixed a bug not allowing the plugin to be Network Activated ([#](http://wordpress.org/support/topic/plugin-code-snippets-network-activate-does-not-create-snippets-tables))

## 1.0 (13 June 2012)
* Stable version released.
