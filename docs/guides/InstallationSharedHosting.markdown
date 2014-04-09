# OpenPhoto / Installation for Shared Hosting

#### OpenPhoto, a photo service for the masses

## Installation on Shared Hosting

This guide instructs you on how to install OpenPhoto on shared hosting sites such as Dreamhost or Bluehost.

Because every webhost is different and features can vary widely from host to host, this guide is written at a high level of abstraction.

If you're using Dreamhost <a href="https://github.com/photo/frontend/blob/master/documentation/guides/InstallationDreamhost.markdown">we have a community-written guide for Dreamhost users</a>. We welcome additions to this guide as well as guides on installing OpenPhoto on your own webhost.

*OpenPhoto should be installed in the root directory of a domain or subdomain.*

Variables:

- *OpenPhotoRoot*: the root directory for OpenPhoto (e.g., ~/openphoto)

### Before you install OpenPhoto
This guide assumes you have:
* Checked that your webhost supports MySQL and PHP
* Shell or FTP access to your web server
* An FTP or SSH client
* A web browser of choice
* A text editor (optional)
* An external cloud service account on Amazon S3 or Dropbox (if you want to store your photos there)


### OpenPhoto Installation Instructions

#### 1. Download OpenPhoto from Github.
Download the source from Github and extract the contents of the *src* folder to your *OpenPhotoRoot* folder. <a href="https://github.com/photo/frontend/archive/master.zip">Direct link to latest version as a .zip file</a>. You can also do the following:

        wget https://github.com/photo/frontend/tarball/master -O openphoto.tar.gz
        tar -zxvf openphoto.tar.gz
        mv frontend-*/src OpenPhotoRoot
        
#### 2. Create the following directories.

        the cache:
        mkdir OpenPhotoRoot/html/assets/cache
        chmod 775 OpenPhotoRoot/html/assets/cache
        
        to store your photos if you're planning on local storage:
        mkdir OpenPhotoRoot/html/photos
        chmod 775 OpenPhotoRoot/html/photos
        
        to store userdata:
        mkdir OpenPhotoRoot/userdata
        chmod 775 OpenPhotoRoot/userdata

You can also do this with your FTP client. If you choose this route, the user and group should have read, write, and execute privileges. World should have read and execute privileges.

#### 3. Install any dependencies or modules needed.
Your webhost may include them or let you install them, so check their documentation. Here's what you'll need:

* The Pecl extension `oauth` for authentication
* ImageMagick or GD for photo rendering

The method of installing these varies by webhost. Some webhosts let you install them by yourself; others will install these for you if you contact them.

#### 4. Create your cloud accounts (if you plan on using them).
Create an account at <a href="https://aws.amazon.com/s3">Amazon AWS</a> or <a href="http://www.dropbox.com">Dropbox</a> if you plan to use them. Create a new bucket (S3) or app (Dropbox). Save your keys since you'll need them soon.  

At Amazon:    
* <a href="https://portal.aws.amazon.com/gp/aws/securityCredentials">Obtain your access keys</a> and save them.

**Note**: OpenPhoto will create a bucket for you during the installation process, so you don't need to do that yet.

At Dropbox:
* Sign in and create a folder for your photos to go in. 
* Visit <a href="https://www.dropbox.com/developers/apps">the developers page</a>
* Select Create an App, and select Core API for App Type and Folder Access.

This will give you a development app to use for your photos. Save your access keys; you'll need them soon.

#### 5. Create a database and user.
Visit your control panel for managing databases and create a new database and new user for the database. Give the user `CREATE DATABASE` privileges if you haven't created the database yet. Remember the hostname (the default should be fine), database name, username, and password.

Your webhost may have a graphical interface such as cPanel or phpMyAdmin that you can do this in.

#### 6. Configure the subdomain or domain.
You may have to add the domain if you're bringing in a new domain. Consult your webhost's documentation if needed. Depending on your webhost you may have to visit multiple areas of the site to configure everything, or you may have to configure these separately. Here's what you need to set up.

* PHP: Select the latest stable version, FastCGI configuration if available
* Web directory: OpenPhotoRoot/html

If you can't set the web directory to OpenPhotoRoot/html through a web interface, you can create an .htaccess file in the root directory. Open a text editor and include the following:

       RewriteEngine on
       RewriteBase /
       RewriteCond %{HTTP_HOST} ^your.domain$ [NC,OR]
       RewriteCond %{REQUEST_URI} !html/
       RewriteRule (.*) /html/$1 [L]
       
Save the file as .htaccess and upload it to the root folder of your site.
        

#### 7. Install OpenPhoto
After waiting a sufficient amount of time for the subdomain name to propagate, use the browser to connect to the new subdomain.  You should see a setup page for OpenPhoto which will allow you to configure your OpenPhoto site.

* Enter your email address and select a password.

* Select your image renderer (ImageMagick or GD are the most common options), database (MySQL or InnoDB), and storage (Local filesystem, Amazon S3, Amazon S3+Dropbox, Local filesystem+Dropbox).

* Enter your credentials for your database, Amazon S3, or Dropbox.

**ENJOY!**

### Troubleshooting

#### Setup page looks strange (black and white, unstyled)
If the setup page is not colorful and well formatted, then the CSS and Javascript files are most likely not being loaded.  Possible causes:

- Web directory root is not properly set (check control panel for the subdomain or your .htaccess file)
- html/assets/cache directory is not writeable by Apache (check your permissions)

#### My webhost doesn't recognize OpenPhotoRoot/html as the index directory.
You can set this in the .htaccess page at OpenPhotoRoot. If your webhost lets you set this through the web panel you can also do that there.

#### Error setting up the database
Double check all the parameters. Check your database control panel and verify that everything is correct. Also double check that the user for your database has permission to create a database if you haven't already created a database.

#### Help! I'm stuck and I have questions!
If you have questions we're always around to help. We've got several contact options listed on the <a href="http://theopenphotoproject.org/contribute">contribute</a> page.
