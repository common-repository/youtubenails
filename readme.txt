=== YouTubeNails ===
Contributors: alvaron
Donate link: http://www.wpworks.wordpress.com/
Tags: youtube,thumbnails,video
Requires at least: 3.0.3
Tested up to: 3.2.1
Stable tag: 3.0.0

== Description ==

Create a dynamic gallery multiple widget(works as shortcode too), with thumbnails of each post with youtube/vimeo(beta) videos displayed on the content linked to the post single. Checks all you video posts, but you can filter them by category and choose the number of posts.

Based on 

Media Library Gallery 1.0.2 (http://www.cybwarrior.com/media-library-gallery/) by Raphael Verchere(http://www.cybwarrior.com)

Video Thumbnails 1.0.7(http://sutherlandboswell.com/2010/11/wordpress-video-thumbnails/) by Sutherland Boswell(http://sutherlandboswell.com)

and

Simple Video Embedder(http://www.press75.com/the-simple-video-embedder-wordpress-plugin/) by James Lao(http://jameslao.com/)

Special thanks to Felipe Caroé http://www.felipecaroe.com/ for suggesting the name!


== Installation ==

See it working on: http://www.felipecaroe.com/galeriavideos/

1. Upload `youtubenails` folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Register a widget sidebar on your functions file, for example, just paste the code below on your theme functions.php

/*if ( function_exists('register_sidebar') )
register_sidebar(array(
	'name' => 'wp_youtubenails',
	'before_widget' => '',
	'after_widget' => '',
	'before_title' => '',
	'after_title' => '',
));*/

Or

You if you have already registered any sidebar, you can drag the `YouTubeNails` widget inside it, at wp-admin

4. Configure the widget on your wp-admin pannel and save(see screenshot 1)
5. Use the PHP code bellow where you want the widget to show, on your theme pages
/* If ( !function_exists('dynamic_sidebar') || !dynamic_sidebar('wp_youtubenails')) : endif; */
6. Always add the youtube video urls on your posts using the "add video" icon. To add object and iframe tags, use the html edition mode.
7. The table id for the result table wp_ytbnstb;

To work as short code, call
[ytbn nop="2" ln="1" catg="" tbsz="1" cpad="3" cpin="3"]

or call it on php as function  youtubenails_show(8,1,'',2,3,3);

where the parameters are

$nop - the number of posts you want to show;
$ln - number of columns on each row;
$catg - a specific category;
$tbsz - the thumbnail type based on YouTube API http://code.google.com/intl/en-UK/apis/youtube/2.0/developers_guide_protocol.html;
$cpad - the result table cellpadding;
$cpin - the result table cellspacing;

== Frequently Asked Questions ==

It`s very easy to use as you see, let me know about doubts and issues alvaron8@gmail.com;

== Screenshots ==

Please let me know about the way you use the plugin, send some screenshots from it to alvaron8@gmail.com

1. Configuring the widget.
2. See it working on http://www.felipecaroe.com/galeriavideos/

== Changelog ==
3.0.0
Supports multiple widgets and shortcodes;
Vimeo supported(beta feature);

2.0.0

Now YouTubeNails is a configurable widget. 


== Upgrade Notice ==
This is the second version, that works as a widget. If you need support for the first version, let me know alvaron8@gmail.com

== Arbitrary section ==
This Plugin supports YouTube and Vimeo(beta)
If you decide to use iframe and embed object, please use the html code insert on the post
The plugin works better when urls are pasted on the post editor

This readme file were validated at http://wordpress.org/extend/plugins/about/validator/