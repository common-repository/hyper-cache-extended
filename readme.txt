=== Hyper Cache Extended===
Tags: cache,chaching,speed,performance,super cache,wp cache
Requires at least: 2.5
Tested up to: 4.9.5
Stable tag: 1.6.3
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=D96ZZLGAV8X8J
Contributors: mlazarov

Hyper Cache Extended is flexible and easy to configure cache system for WordPress. It's aim is to work on any installation.

== Description ==

Hyper Cache Extended is a new cache system for WordPress, specifically written for
people which have their blogs on low resources hosting provider 
(cpu and mysql). It works even with hosting based on Microsoft IIS (just tuning
the configuration). It has three invalidation method: all the cache, single post
based and nothing but with control on home and archive pages invalidation.
Hyper Cache Extended is based on original wordpress plugin "Hyper Cache" wich is
writen by Satollo (http://wordpress.org/extend/plugins/hyper-cache)

It has not yet tested for multisite configuration (WordPress 3.0 feature).

Some features:

* compatible with the plugin wp-pda which enables a blog to be *accessible from mobile devices*
* manages (both) *plain and gzip compressed pages*
* autoclean system to reduce the disk usage
* 404 caching
* redirects caching
* easy to configure
* Global Translator compatibility
* Last Modified http header compatibility with 304 responses
* compressed storage to reduce the disk space usage
* agents, urls and cookies based rejection configurable
* easy to integrated with other plugins
* option to move cache to other partition/disk
* only serve cached pages when web server average load is above a certain number

More can be read on the [official plugin page](http://marto.lazarov.org/plugins/hyper-cache-extended) and write me
if you have issues to lazarov@mail.bg

Contribute to project:
http://github.com/mlazarov/Hyper-Cache-Extended


Thanks to:

* Satollo which is the creator of Hyper Cache
* Amaury Balmer for internationalization and other modifications
* Frank Luef for german translation
* HypeScience, Martin Steldinger, Giorgio Guglielmino for test and bugs submissions
* Ishtiaq to ask me about compatibility with wp-pda
* Gene Steinberg to ask for an autoclean system
* Marcis Gasun (fatcow.com) for Bielorussian translation
* many others I don't remember

== Installation ==

1. Put the plugin folder into [wordpress_dir]/wp-content/plugins/
2. Go into the WordPress admin interface and activate the plugin
3. Add **define("WP_CACHE",true);** to wp-config.php just after the **define("WPLANG", ...);**.
4. Optional: go to the options page and configure the plugin

Before upgrade DEACTIVATE the plugin and then ACTIVATE and RECONFIGURE!

== Frequently Asked Questions ==

**How can I submit a bug?**

Contact me at martin@lazarov.bg - it's the quickest way to have it fixed. You can post to the WordPress forum too but I read it rarely.


**What is Max Server Load Average?** 

If the `Server load` is above `Max server load average` then the plugin will serve only cached version and will not try to create new cache file until the server load is bellow `Max server load average` value.
You can [read more about this in bulgarian](http://marto.lazarov.org/plugins/hyper-cache-extended/max-server-load-average)

**Is it possible to exclude caching on certain pages with Hyper Cache Extended**

Yes! You can use `URI to reject` text box to enter URL's that will not be cached!
Use with caution - not allowing HCE to cache can lead to slow WordPres experience

**Do do the HCE has option to automatically delete the expired cache?**

 You can click on “Enable” for “Cleaning process” – “Cleaning process – Enable/Disable auto purging of old files. Enable cleaning process to remove expired cache. This will free some space, but it’s better to keep this Disabled”.



== Changelog ==
= 1.6.0 =
* Adding smart home caching feature

= 1.5.0 =
* Adding screenshosts section

= 1.4.0 =
* Updating mobile user agents list (Thanks to Stoyan Stanev)

= 1.3.0 =
* Disabling cleanup process when server is above max load average
* Fixing wrong used reject config item
* A zero (or less) value means a cached page is valid forever

= 1.2.0 =
* Adding default (optimal) value for max load average

= 1.1.1 =
* Install instructions update

= 1.1.0 =
* Adding WP_CACHE check

= 1.0.5 =
* Adding HTTP_HOST to cache file name

= 1.0.4 =
* Fixing rejected urls bug (10x to Robert)

= 1.0.3 =
* Fixed conflict with zlib.output_compression and HCE deflate support
* Fixing "Max server load average" config description (10x to scoobydoo)

= 1.0.1 =
* Fixed cached pages timeout bug
* Added advanced-cache.php version check

= 1.0.0 =
* New cache directory outside of Hyper Cache Extended plugin home directory. Now cache files will NOT be removed when upgrading Hyper Cache Extended.
* Fixed bug which causes incorect is_feed check
* Now hyper cache extended uses only advanced-cache.php config (config is replaces when upgrading)

= 0.9.9 =
* Bugfixes

= 0.9.8 =
* Updated warning message

= 0.9.7 =
* Added warning to inform when server load goest over "Max server load average" config option

= 0.9.6 =
* Short tag Bugfixes (10x to joanne123)

    
== Screenshots ==
1. Cache Status
2. Base Configuration
3. Mobide Devices Configuration & Compression
4. Advances Options

