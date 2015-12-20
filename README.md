# Smudge & Clean

This repository was created to provide an example for the blog post ["Git Smudge and Clean Filters"](http://www.michaelclark.x10host.com/wp/2015/12/20/git-smudge-and-clean-filters/)

## To run the example ##

What we're trying to accomplish here is to have a web.config or app.config with config values for local development (like Amazon Keys) but that are not available on GitHub.  

The .clean filter will be used to empty the Values of the configs whenever you **CHECK IN** (Push to the repo).  

The .smudge will be used to set the values of the config whenever you **CHECK OUT**.

To test it properly:

1. Clone the repo
2. Run the example by executing the "setup.sh" file. 
3. Note that in your repository there should be a file here: ".git/config" with the smudge and clean filters referenced in the file.
4. Note that your web.config & app.config in the "TestConfigs" directory should now be "Smudged" (have the values of the .smudge)
5. Modify the config values of the configs in the TestConfigs directory.
6. Push to your repository (feel free to fork this)
7. Note that the commit that you pushed does not contain config values (thanks to the .clean)
