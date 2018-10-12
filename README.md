# Change Order of Review Cards in Regular Decks

*Change Order of Review Cards in Regular Decks* is an Anki add-on which orders review cards in regular decks by interval.  By default reviews are sorted in order of decreasing intervals however it can be configured to sort by increasing intervals as well.  It is compatible with:

* Anki v2.0
* Anki v2.1 with the default scheduler
* Anki v2.1 with the [experimental v2 scheduler](https://anki.tenderapp.com/kb/anki-ecosystem/experiment-scheduling-changes-in-anki-21)

## Installation

To install follow the instructions on the AnkiWeb [add-ons page](https://ankiweb.net/shared/info/3731265543).

## Configuration

Configuration is via setting `order` in the source file.  The following options are available:

* `order = "ivl desc"` : Order reviews by decreasing interval.  This is the default.
* `order = "ivl asc"` : Order reviews by increasing interval.

## Known Issues

Please note that this add-on may significantly slow down queue building, especially if you have a large backlog and a slow computer.  You may wish to use a filtered deck instead which can more efficiently sort a large backlog and can be used on the mobile and online clients as well.

*Keep in mind that under Anki 2.0 and Anki 2.1 with the default scheduler filtered decks behave in an unexpected manner.* It's often suggested that new users avoid the use of filtered decks for this reason.  These behaviors are documented in the [Anki Manual](https://apps.ankiweb.net/docs/manual.html#home-decks):

> In the current implementation, if you create, rebuild, empty or delete a filtered deck while cards are still in learning, they will be turned back into new cards. In the case of failed reviews in relearning, any remaining relearning steps will be skipped.

If you are using Anki 2.1 with the experimental v2 scheduler you do not have to worry about these behaviors as documented [here](https://anki.tenderapp.com/kb/anki-ecosystem/experiment-scheduling-changes-in-anki-21).

> Filtered decks no longer reset (re)learning cards when they are built or emptied, and reviews and learning cards will show up in the correct queue instead of the new queue.


## Bugs and Support

If you encounter a bug or need support please see the official [README](https://github.com/xquercus/change-order-of-review-cards). Please report bugs through [github](https://github.com/xquercus/change-order-of-review-cards/issues).  Please don't use the review section of the AnkiWeb add-on page for support as I won't receive a notification and there is no way for me to respond.

## Revision History

* Updated 2018-10-12:

    * Added support for the [experimental v2 scheduler](https://anki.tenderapp.com/kb/anki-ecosystem/experiment-scheduling-changes-in-anki-21).

* Updated 2018-08-13:

    * Added 2.1 support. It will only alter the normal scheduler - if you are using the experimental scheduler, you can accomplish the same behaviour with better performance and mobile device support by using filtered decks instead.
