# Server configuration

<p class="uk-article-lead">Pagekit will run on all common web servers.</p>

## Apache 2.2+

Although Pagekit should run fine on Apache 2.2+ without additional configuration, during installation you may receive a warning message. If you do, you should verify that the `.htaccess` file is present in the root of your Pagekit folder.

**Note** The `.htaccess` file is the Apache configuration file and is a hidden file on Unix-based systems; as such it may not have been unpacked. If it is not present, copy it from the Pagekit packager.

It is possible as well that your webserver does not allow the server's configuration to be overridden through an `.htaccess` file. In that case, contact your hosting provider and ask them to change the AllowOverride directive.

Another common problem is that the `mod_rewrite` module is not enabled on your webserver, in which case you'll also have to turn to your hosting provider to have them enable this Apache module. If the module is not available, Pagekit will still work but fall back to a URL format of the form `http://example.com/index.php/page/welcome`.