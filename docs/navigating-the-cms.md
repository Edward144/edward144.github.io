# Navigating The CMS

Here we will go over each section within the CMS and explain how to use it. You can find a link to each primary CMS section in the navigation menu. 

To start with we will go over the login pages and general layout of the CMS once you have logged in.

## Login pages

There are three main pages as part of the log in system: the main login form, the password reset request form, and the reset password form.

### Admin login

![Admin login screen](_images/_navigating-the-cms/admin-login.png)

At the top of the page is a **Return to site** link. This will take you to the homepage of the public facing website. 

Within the form itself is a username and password field which are self explanitory. Fill these in with the correct details and click **Sign In** to sign in. If your details are correct then you will be redirected to the CMS dashboard screen, otherwise an error message will be displayed explaining that the username or password is incorrect.

Next to the **Sign In** button is a **Forgotten password?** link, clicking this will take you to the [password reset request form](#password-reset-request).

Finally at the bottom of the page is the **Powered by Clover CMS** link, clicking this will take you to the [github page](https://github.com/Edward144/Clover-CMS). 

### Password reset request

![Admin login screen](_images/_navigating-the-cms/reset-request.png)

As with the login page, at the top of the page is the **Return to site** link and at the bottom is the **Powered by Clover CMS** link.

To the right of the Request Reset button is a **Return to login** link, this will take you back to the main login page.

To reset your password simply fill in the email address associated with your user login. If the email address exists within the database then a reset link will be sent to it. 

The form will display a message explaining that the email will be sent if the email exists whether it does or not. This is for security purposes to prevent wrongful use by entering emails to work out if they exist. 

The reset link which has been sent will be valid for 24 hours and will expire after this time. It will also automatically be marked as expired as soon as it is clicked. So you should make sure to update your password as soon as you click the link, otherwise you will need to request a new link.

### Reset password

![Admin login screen](_images/_navigating-the-cms/reset-password.png)

Once you have clicked the link within the email that was sent to you, you will be taken to the reset password page. This page also features the **Return to site**, **Powered by Clover CMS** and **Return to login** links.

Fill out a new password in both the Password and Confirm Password boxes and click update password. You password must contain at least one lower case letter, one uppercase and a number. 

You can also click the Generate Password button which will fill in both fields and display the generated password for you to keep note of. This button isn't always perfect and can sometimes generate a password which doesn't contain each of the three character types. If this happens simply click it again to generate a new password. 

Once you have set your new password it will be changed immediately, you can now return to login and sign in with the new password.

## CMS layout