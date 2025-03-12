# ⟡ Michigan Creative Drupal Install Profile
An easier way to add our recommended modules to a new site from Pantheon.

## How to install
If you are using the Creative CLI tool to install a Pantheon Drupal site, installing a site with this profile happens automatically.

If you need to install this manually, do these steps first
1.
```bash
$ mkdir web/modules/custom
$ git clone git@github.com:m-creative-web/creative-paragraphs.git web/modules/custom/creative_paragraphs
$ rm -rf web/modules/custom/creative_paragraphs/.git
$ git clone git@github.com:m-creative-web/creative-custom.git web/modules/custom/creative_custom
$ rm -rf web/modules/custom/creative_custom/.git
```
2. 
```bash
$ mkdir web/themes/custom
$ git clone git@github.com:m-creative-web/creative-drupal-theme.git web/themes/custom/creative
$ rm -rf web/themes/custom/creative/.git
```
3. 
```bash
$ mkdir web/profiles/custom
$ git clone git@github.com:m-creative-web/creative-drupal-profile.git web/profiles/custom/creative_starter
$ rm -rf web/profiles/custom/creative_starter/.git
```
4. Make sure the root composer.json file is requiring core verison 10 and not 9.
```bash
$ lando composer update --with-all-dependencies
```
5. Install Drupal using our installation profile