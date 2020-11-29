FlexForms Extras for PHP
========================

FlexForms Extras adds the most commonly used best-of-class Javascript components to the already excellent [FlexForms](https://github.com/cubiclesoft/php-flexforms).  Choose from a MIT or LGPL license.

[FlexForms](https://github.com/cubiclesoft/php-flexforms) is the culmination of seven years of precision software development boiled down into a little over 1,200 lines of code ready for your next web application.  The core functionality is trusted and has been deployed widely throughout the world.  FlexForms Extras expands upon FlexForms with the most commonly used Javascript components used to bring administrative interfaces to life such as [Admin Pack](https://github.com/cubiclesoft/admin-pack).

[![Donate](https://cubiclesoft.com/res/donate-shield.png)](https://cubiclesoft.com/donate/) [![Discord](https://img.shields.io/discord/777282089980526602?label=chat&logo=discord)](https://cubiclesoft.com/product-support/github/)

Features
--------

* Date picker.
* Accordions.
* Multiselect tags support.  Adds select2 in tag mode for selecting multiple items.
* Multiselect dropdown support.  Adds a jQuery UI widget for selecting multiple items.
* Multiselect flat view support.  Adds a jQuery UI widget for selecting and reordering multiple items.
* Table row ordering.  Adds drag-and-drop support to an injected column for the 'table' type.
* Table cards.  Adds responsive layout support for the 'table' type via client-side templates to convert tables into formatted cards in a new table column so each row fits on a single screen horizontally.
* Table scrolling.  Adds scrolling of a table body to fit an entire table onto a single screen vertically.
* Table sticky headers.  Adds sticky header support to the header for the 'table' type.  Buggy on mobile OS platforms (e.g. Android Google Chrome).
* Has a liberal open source license.  MIT or LGPL, your choice.
* Designed for relatively painless integration into your project.
* Sits on GitHub for all of that pull request and issue tracker goodness to easily submit changes and ideas respectively.

Usage
-----

The following new field types are added:

* date - Adds a jQuery UI datepicker field.
* accordion - Adds a jQuery UI accordion with the specified "title".

New string types:

* endaccordion - Closes an open accordion type.
* nosplit - Items in accordions have a visual splitter.  This allows items to be better grouped visually.

New type-specific options for array fields:

* options (date) - An array of options to pass to [jQuery UI datepicker](http://api.jqueryui.com/datepicker/).
* callbacks (date) - An array of Javascript callbacks to pass to [jQuery UI datepicker](http://api.jqueryui.com/datepicker/).
* options (accordion) - An array of options to pass to [jQuery UI accordion](http://api.jqueryui.com/accordion/).
* callbacks (accordion) - An array of Javascript callbacks to pass to [jQuery UI accordion](http://api.jqueryui.com/accordion/).
* mininput (select + tags mode) - An integer specifying the number of characters that need to be entered before showing matching items in the dropdown.
* multiselect_options (select + all new modes) - An array of options to pass to [select2](http://api.jqueryui.com/accordion/) for tags mode, [jQuery multiselect widget](http://www.erichynds.com/blog/jquery-ui-multiselect-widget) for dropdown mode, and [jQuery UIX multiselect](https://github.com/yanickrochon/jquery.uix.multiselect/wiki/API-Documentation) for flat mode.
* multiselect_callbacks (select + all new modes) - An array of Javascript callbacks to pass to [select2](http://api.jqueryui.com/accordion/) for tags mode, [jQuery multiselect widget](http://www.erichynds.com/blog/jquery-ui-multiselect-widget) for dropdown mode, and [jQuery UIX multiselect](https://github.com/yanickrochon/jquery.uix.multiselect/wiki/API-Documentation) for flat mode.
* order (table) - A string to display as the column header for the drag-and-drop column.
* order_options (table) - An array of options to pass to [TableDnD](https://github.com/isocra/TableDnD).
* order_callbacks (table) - An array of Javascript callbacks to pass to [TableDnD](https://github.com/isocra/TableDnD).
* card (table) - A string or an array of options to pass to [TableCards](https://github.com/cubiclesoft/jquery-tablecards).
* cardwidth (table) - An integer representing the number of pixels the width of the table has to fall below before switching to card mode.  The default is to switch to card mode if the table exceeds its parent element.
* cardhead (table) - A string containing the table header field to display.  The default is to hide all headers.
* card_options (table) - An array of options to pass to [TableCards](https://github.com/cubiclesoft/jquery-tablecards).
* card_callbacks (table) - An array of Javascript callbacks to pass to [TableCards](https://github.com/cubiclesoft/jquery-tablecards).
* bodyscroll (table) - A boolean that indicates whether or not to enable responsive table body scrolling.
* bodyscroll_options (table) - An array of options to pass to [TableBodyScroll](https://github.com/cubiclesoft/jquery-tablebodyscroll).
* bodyscroll_callbacks (table) - An array of Javascript callbacks to pass to [TableBodyScroll](https://github.com/cubiclesoft/jquery-tablebodyscroll).
* stickyheader (table) - A boolean that indicates whether or not to use sticky table headers.
* stickyheader_options (table) - An array of options to pass to [StickyTableHeaders](https://github.com/jmosbech/StickyTableHeaders).
* stickyheader_callbacks (table) - An array of Javascript callbacks to pass to [StickyTableHeaders](https://github.com/jmosbech/StickyTableHeaders).

Known Limitations
-----------------

Font sizes inside an accordion are different from the font sizes outside the accordion.

The multiselect dropdown and multiselect flat widgets have identical Javascript names and are therefore incompatible.  As a result, FlexForms Extras does not allow both to be used on the same page.  Instead, use the tags mode widget and the flat widget together.

Most of the multiselect widgets have problems with optgroups.  Instead of using optgroups, prefix a short string to each string displayed to the user.

The table features won't activate if the "formtables" state is set to false.  This makes sense since tables are converted to vertical div-based output.

Sticky Table Headers has known browser lag issues outside of table scrolling when working with thousands of rows of data.
