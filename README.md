This plugin adds the "Sign-in with Google / Facebook / Github / Linkedin / Windows Live" buttons on the login page. The first time the user login with a social account, a new Moodle account is created. 

### Installation:

1. add the plugin into /auth/googleoauth2/
2. in the Moodle administration, enable the plugin (Admin block > Plugins > Authentication)
3. in the plugin settings, follow the displayed instructions.

To add to login, add the following to `login/index.php` before `echo $OUTPUT->footer()`:

```php
require_once($CFG->dirroot . '/auth/googleoauth2/lib.php'); 
auth_googleoauth2_display_buttons();
```

### Support and maintenance
More information on the [official web site](http://mouneyrac.github.io/moodle-auth_googleoauth2/).

### Credits
* [Contributors](https://github.com/mouneyrac/auth_googleoauth2/graphs/contributors)
* [CSS social buttons](http://zocial.smcllns.com/)
