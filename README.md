# dev-dissallow-search
A guide to using best practice methods to remove an internet-facing development site/environment from being indexed by search engines - in particular Google

- Password protect the directory
  - cPanel method
  - .htaccess method
- Use robots.txt
- Use the robots index.html meta tag
- Google Search Consol

## Password protect the directory

### cPanel method

Log into the cPanel, konsoleH, or whatever server/environment management tool, set a password on the directory you would like to hide from search engines

### .htaccess method

Refer to this [link](https://davidwalsh.name/password-protect-directory-using-htaccess)

## Use the robots.txt

Structure your robots.txt like this:

```shell
# Don't allow web crawlers to index anything
User-agent: *
Disallow: /
```

Place the robots.txt in the directory you wish to hide from search engines

## Use the robots index.html meta tag

Put the following meta tag into the <head> of your index.html file

```shell
<meta name="robots" content="noindex">
```

## Google Search Consol

Set your site up on [Google Search Consol](https://www.google.com/webmasters/tools/). Once set up, use the 

- Go to the **Remove outdated** content page
- Enter the URL (web address) of the page that you want to remove
- Select **Request removal**
