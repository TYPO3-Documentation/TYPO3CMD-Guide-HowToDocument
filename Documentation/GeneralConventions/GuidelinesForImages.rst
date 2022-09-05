.. include:: /Includes.rst.txt
.. highlight:: rst
.. index::
   ! Images
   Screenshots
   see: Screenshots; Images
.. _guidelines-for-images:

==============================
Guidelines for creating images
==============================

When embedding images with reST, please add a shadow,
as described in :ref:`how-to-document-images`.

There are various kinds of images used in the documentation. The most
common are:

#. Screenshots
#. Screenshots, augmented with graphic elements, the most common being
   arrows, texts, boxes and numbers to highlight parts of the screenshot,
   add extra explanation etc., with the intention of making the image more
   useful for the reader
#. Diagrams, such as UML diagrams


.. index:: Images; Style guide

General guidelines
==================

*  In general, comply with the
   `TYPO3 web style guide <https://styleguide.typo3.org/patternlab/public/index.html>`__


.. index:: Images; Fonts

Texts & fonts
-------------

*  When using fonts, please use recommended: **Primary font: "Source Sans Pro", "Helvetica", "Arial",
   sans-serif;**. You can download "Source Sance Pro" as TTF files:
   `Assets <https://styleguide.typo3.org/Data/TYPO3_Assets_2017-08-23.zip>`__,
   path: :file:`00\ -\ Assets/Fonts/SourceCodePro-Regular.ttf`
*  If you use text in an SVG, make sure it can be
   displayed on systems that have not installed the used font.
   There are a
   number of ways to do this. If in doubt, ask for :ref:`help <help>` or save the image
   as bitmap (.png). However, if SVG is used, the image can be scaled
   better.
*  In any case, you should be safe with using a commonly supported font
   like Helvetica or Arial. Remember, the Web Style Guide proposes
   *Source Sans Pro, Helvetica, Arial*.


.. index::
   Images; Formats
   Images; PNG
   Images; SVG

Image formats
-------------

*  It is recommended to use PNG for bitmaps (for example screenshots, photographs)
   and SVG for vector graphics images. In any case, you can use .png.

.. index:: Screenshots; Guidelines

Guidelines for screenshots
==========================

*  use PNG format (.png file ending)
*  Do not use huge full screen screenshots (except in some cases where it makes sense,
   for example when describing the various parts of the backend). Select a portion
   of a screen that will reflect what you are trying to show. To save yourself hassle,
   use a screenshot tool which can create a screenshot of a portion of a screen.

Here are some :ref:`examples for screenshots <t3contribute:how-to-see-merge-conflicts>`.



.. code-block:: rest

   .. image:: images/github-getting-started-raw.png
      :class: with-shadow
      :scale: 70

How it looks:

.. image:: images/github-getting-started-raw.png
   :class: with-shadow
   :scale: 70

Another example:

.. image:: images/backend-raw.png
   :class: with-shadow
   :scale: 70


You may however notice, that it might be helpful to point out some relevant part of the
screenshots. That is what we do by creating images as described in the next section.


.. index:: Screenshots; Adding graphics elements

Guidelines for screenshots with graphics elements
=================================================

You will often see a screenshot where additional graphic elements have been added in the
documentation. These additional graphic elements may be boxes, numbers or arrows. Up until,
we did not have guidelines for this, so you may see various shapes in different colors.

.. important::
   This still needs some work. If you plan on adding images to a manual, contact
   us in the #typo3-documentation channel. Help with optimizing this section is also
   appreciated.


.. index::
   pair: Screenshots; Icons
   pair: TYPO3; Icons

To get the icons
----------------

Either download the zipfile and extract it.
You can find the download link on https://github.com/TYPO3-Documentation/Images,

Or clone the repository:

.. code-block:: bash

   git clone https://github.com/TYPO3-Documentation/Images


The icons will be in images/final/icons.


Follow these guidelines
-----------------------

*  Icons are used for numbers and arrows. The size of the icons should not be changed.
*  Simple frames are TYPO3 Orange (#F49700) and have a line thickness of 2 px and a
   corner radius of 2 px.
*  Text fields are TYPO3 Orange (#F49700) and have a corner radius of 2 px.
*  Dividing surfaces have a 2px frame in TYPO3 Orange (#F49700) with a corner radius
   of 2 px.
*  Icon shadows have an

   * horizontal offset of 4 px
   * vertical offset of 4 px
   * blur radius of 10 px
   * spread radius of 0 px
   * color of RGBA (0, 0, 0, 0.3)


Examples
--------


.. figure:: images/backend-with-boxes.png
   :class: with-shadow

   PNG Image with rectangles and numbers

.. figure:: images/backend-with-boxes-2.svg
   :class: with-shadow

   SVG image with rectangles and numbers

.. figure:: /Images/edit_me_on_github+shadow.svg
   :class: with-shadow
   :alt: Image with arrow

   SVG Image with arrow
