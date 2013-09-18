# OpenSpending - WordPress plugin

WordPress plugin to make openspendingjs visualisations easy to add to WordPress posts and pages.

## Installation

1. Add the openspending directory into your WordPress instance's plugin
   directory (usually *wp-content/plugins/*).
2. Go to your admin panel, navigate to plugins, find OpenSpending and
   activate it.

### Non-standard WordPress setup?

If you have set WordPress up a bit differently, e.g. placed the wp-content directory someplace else you might have to help the plugin find *wp-load.php*.

In the file:

    wp-content/plugins/openspending/code/load-wordpress.php

you will need to uncomment a line saying:

    // define('WP_LOAD_PATH', '/path/to/wp-load.php');

and put in the absolute path to wp-load.php

This is only if you've done something special to your WordPress setup!

## How to Use

The OpenSpending WordPress plugin operates using the standard WordPress *shortcodes*, namely:

    [openspending]

Three attributes **must** be defined:

* *type* - The type of visualisation to use
* *dataset* - The dataset on openspending.org to use
* *drilldowns* - Dimensions of the dataset to drill down into

If you would like to add a *treemap* for the dimensions *from* and *to* in the [*ukgov-25k-spending* dataset](http://openspending.org/ukgov-25k-spending) on OpenSpending the only thing you need to add to your post or page is:

    [openspending type="treemap" dataset="ukgov-25k-spending" dimensions="from,to"]

## Supported Visualisations

* Treemap (type: "treemap")
* Bubbletree (type: "bubbletree")
    * Supported icons/colors for COFOG
