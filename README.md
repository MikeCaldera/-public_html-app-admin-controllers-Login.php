# -public_html-app-admin-controllers-Login.php
TastyIgniter - the user will see an error message on the login page indicating that the login attempt was unsuccessful.
We do this to let the user know what's going on or status. Yes, Ratelimiting protection is now added... to the login side as well as other functions. (See Ratelimiting)
I did this here so that updates won't break this or by adding another theme.
/app/admin/controllers/Login.php
In this example, an error flash message is added using flash()->error() when the authentication fails. The error message is retrieved from the language file (lang('admin::lang.login.alert_failed_login')). After adding the flash message, the user is redirected back to the login page using return $this->redirectBack().

Make sure to replace 'admin::lang.login.alert_failed_login' with the appropriate key from your language file that represents the error message you want to display.

With this modification, when the authentication fails, the user will see the error message on the login page indicating that the login attempt was unsuccessful.


*** requires this file to be updated /vendor/laravel/framework/src/Illuminate/Routing/Middleware/ThrottleRequests.php see throttlerequests
