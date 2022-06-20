# Initial Set Up

## Installation

Installing Clover CMS is as simple as downloading a copy of the files, you can view the latest releases [here](https://github.com/Edward144/Clover-CMS/releases), and then copying them to your web server.

It is recommended that you installed the cms in the document root of your server for the simplest set up, however it is possible to install it to a sub-directory with some additional configuration.

If you wish to install into a sub directory then you will want to make sure that the RewriteBase location within the `.htaccess` file points towards your sub-directory. For example if the path to your installation was **/home/user/public_html/my-site1/** then your `.htaccess` file would look like this:

    RewriteEngine on
    RewriteBase /my-site1/

Once you have copied the cms files to the desired directory on you web server you will need to ensure that the permissions are set correctly. If the permissions have not been correctly configured then the basic configuration will fail to complete and you may run into additional issues down the line.

The file permissions required will vary depending on your web servers specific configuration, however as a general rule folders should be set to `775/755` permissions and files to `664/644`.

> `775` and `664` permissions will likely be what you need if you are running a non PHP-FPM configuration where the web user owns the document root directory (www-data, httpd, apache).

> `755` and `644` permissions will be suitable for PHP-FPM installations where each user has their own web root directory within their home directory.

Now that your files have been configured it is time to move on to the MySQL database. All you will need to do is create a new empty database and ensure that a user is configured to have access to that database.

Once the database has been created you can move onto the basic configuration, where all of the required tables will be automatically created.

## Basic configuration

To start the basic configuration of Clover CMS head to your website and the directory where you have installed the CMS e.g. https://yoursite.com. You should automatically be redirected to the set up page. On this page start by filling out your database connection details, and then fill in an email and password for the initial admin user.

Assuming your file permissions and database have been set up correctly the configuration will complete without errors and you will see a message confirming completion. This message will link you to the admin login page which can be found at https://yoursite.com/admin-login.

You will also be sent an email to the provided address to confirm that you have been set up as a new user, with details of how to login including your username, which for the initial user will always be **admin**.

## Additional files

Clover CMS is built upon Bootstrap 5.0.2 and the Bootstrap files are included within the **node_modules** directory by default. This has changed since previous versions where Bootstap was omitted. You may wish to delete the **node_modules** directory in order to save space if you do not plan on modifying the Bootstrap configuration. Assuming you have NPM installed Bootstrap can always be installed by running:

    npm install bootstrap@5.0.2

You may also wish to delete the **scss** directory. The SCSS files have been used in conjunction with the default Bootstrap SCSS files to generate the two default CSS files `admin.min.css` and `style.min.css`.

It is recommended that you create and include your own custom CSS files which are included after the default one. This will provide you with the option to override default styles without modifying the original files. As such you will not need those SCSS files.