[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/drupal-tome/netlify-template)

# Modified template from Samuel Mortenson using DDEV as localhost

This project is a great place to start for building new Tome projects on Netlify.

To get started, click the "Deploy to netlify" button above and deploy a copy of
this template to Netlify.

# Requirements

- [DDEV](https://ddev.com/)

# Local usage

To install Tome locally, run:

```bash
ddev start
ddev composer install
ddev drush site-install
ddev drush en tome
ddev drush tome:import
```

then run:

```
ddev launch $(ddev drush uli)
```

and click the link to start editing content!

When ready to export your site to Netlify

```
ddev drush tome:export
ddev drush tome:static
```

Commit the changes, which should include cofiguration changes and static html pages.

Push the branch to remote. The build process on Netlify will then import the static html files
