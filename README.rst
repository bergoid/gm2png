gm2png
======

This script is based on Alexander Honda's ``googlemap2png`` script (https://code.google.com/p/googlemap2png/).

Requires:

- ``rabot`` (https://github.com/bergoid/rabot).
- ``wget`` (https://www.gnu.org/software/wget/).
- ImageMagick's ``montage`` tool (http://www.imagemagick.org/script/montage.php).

The output of ``gm2png --help``:
::

    Usage: gm2png TYPE Z XMIN XMAX YMIN YMAX [FILENAME_PREFIX] [LANG]

    'gm2png' downloads individual tiles from Google Maps, stitches
    them together to form a mosaic and saves the result in a .png file.

    TYPE is either 'sat' for satellite imagery, 'ter' for terrain or
    'map' for roadmap.

    Z is the zoom level.

    The tiles to be downloaded form a rectangular area determined by
    XMIN, XMAX, YMIN and YMAX. The top left tile is at (XMIN,YMIN)
    and the bottom right tile at (XMAX, YMAX).

    If FILENAME_PREFIX is specified, the filename of the saved .png
    file will start with FILENAME_PREFIX, followed by the values of
    the other arguments.

    The optional argument LANG allows you to change the annotations on
    the map to another language, if available. If you want to specify
    LANG without specifying FILENAME_PREFIX, use '-' for the latter.

    Examples:

    Creating a roadmap:

        $ gm2png map 15 16831 16834 10903 10907

    The same roadmap, but with some annotations in Dutch instead of English:

        $ gm2png map 15 16831 16834 10903 10907 - nl
