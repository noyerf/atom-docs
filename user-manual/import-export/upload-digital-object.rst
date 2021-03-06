.. _upload-digital-object:

======================
Upload digital objects
======================

:term:`Digital objects <digital object>` objects are computer files that can be
uploaded into and displayed by AtoM; they can include scanned images,
digital photographs, sound and moving image files, and other scanned or
born-digital items. AtoM allows the user to link a single :term:`digital object`
to an :term:`archival description`, or import multiple digital objects to new
lower :term:`levels of description <level of description>`. In AtoM,
there is a 1:1 relationship between a digital object and an
:term:`information object` - meaning every digital object
must be associated with an :term:`archival description`, typically at the file
or item level (see :term:`level of description`).

For every object uploaded, AtoM creates two derivative objects from the
:term:`master <master digital object>`: a :term:`thumbnail` image and a
:term:`reference display copy` of the object. The master digital object is the
unaltered version of a :term:`digital object` that has been uploaded to
AtoM. Note that only authenticated (i.e. logged-in) users may view master
digital objects by default (though this can be changed by editing the
permissions of unauthenticated users - for more information, see:
:ref:`edit-user-permissions`).

.. IMPORTANT::

   By default, **all** users can view the :term:`master digital object` of an
   uploaded PDF, regardless of the "View master" settings in the Archival
   description permissions tab. This is because the reference display copy is
   not large enough to be useful without access to the full PDF, while the
   reference copy might be perfectly serviceable for an image (and restricting
   access to the master may be part of the required copyright conditions).
   Note that users could still restrict public access to uploaded PDFs using
   the PREMIS actionable rights module - for more information, see:
   :ref:`rights`.

.. image:: images/carousel.*
   :align: center
   :width: 70%
   :alt: A image of the carousel in AtoM

At higher :term:`levels of description <level of description>`, the
:term:`view page` of a :term:`parent record` will include
:term:`thumbnails <thumbnail>` of all digital objects registered at lower levels.
The thumbnails are displayed using a :term:`carousel viewer <carousel>` so you
can easily scroll through the set using your mouse or keyboard's arrow keys.
Clicking on a thumbnail will redirect you to the :term:`view page` for the
:term:`description <archival description>` associated with that digital
object. If more than 10 digital objects appear at lower levels, AtoM will
display the first 10 in the :term:`carousel` and provide a link to a digital
object browse page to explore the rest if desired. For more information,
see the :ref:`recurring-carousel` entry in :ref:`navigate`.

.. TIP::

   The digital object carousel can also be disabled by an
   :term:`administrator` via **Admin > Settings > Default page elements**. For
   more information, see: :ref:`default-page-elements`.

See below for more information on:

* :ref:`Linking single digital objects <link-digital-object>`
* :ref:`Uploading multiple digital objects <upload-multiple-objects>`
* :ref:`Uploading PDFs <upload-pdf>`
* :ref:`Editing digital objects <edit-digital-object>`
* :ref:`rename-digital-object`
* :ref:`Deleting digital objects <delete-digital-object>`
* :ref:`Digital object storage <digital-object-storage>`
* :ref:`Supported file formats <file-formats>`

.. seealso::

   * :ref:`rights`
   * :ref:`rights-digital-object`
   * :ref:`manage-digital-object-storage`
   * :ref:`upload-limit`
   * :ref:`rename-title-slug`

.. _link-digital-object:

Link a single digital object to an archival description
=======================================================

A single :term:`digital object` can be linked directly to an existing
:term:`archival description` in AtoM via the "Link digital object" option.
Users can either upload a digital object, or link to an existing resource
available on the web. Instructions on how to do both are included below.

.. NOTE::

   Only **one** digital object can be linked to an archival description at a
   time. If you wish to upload or link multiple digital objects, you will
   need to create lower levels of description. AtoM includes a workflow to
   automate the creation of these lower levels - see
   :ref:`upload-multiple-objects` for more information.

.. image:: images/link-digital-object.*
   :align: center
   :width: 80%
   :alt: A image of the link digital object edit page

To link a single :term:`digital object`:

1. Navigate to the :term:`view page` of an existing
   :term:`archival description` in AtoM. You can do this by
   :ref:`browsing <browse>` or by :ref:`searching <search-atom>` for a specific
   archival description - see :ref:`access-content` for more information on
   navigation in AtoM.
2. Click on the "More" button in the :term:`button block`; from the menu that
   appears, select "Link digital object".

.. image:: images/more-menu-link.*
   :align: center
   :width: 80%
   :alt: A image of the more menu, with the Link digital object option selected

3. AtoM will redirect you to the link digital object :term:`edit page`. Users
   can either upload a digital object, or link to an existing digital object
   available on the internet.

.. image:: images/link-digital-object.*
   :align: center
   :width: 80%
   :alt: A image of the link digital object edit page

4. **To upload a digital object locally**, cick the "Choose File" button to
   navigate to and select a file on your computer or device. Click "Open" once
   the item has been selected from the window that will appear.
5. **To link to an object on the internet**, enter the URL to the external
   object to which you wish to link.

.. IMPORTANT::

   To link to a digital object via the web, you **must** enter a URL that
   ends with the file extension of the resource to which you are trying to
   link - for example, to link to an image, the URL should end with .jpg,
   .png, etc. You can usually get to this URL by clicking on the resource
   directly, or by right-clicking and selecting "View image" etc in your
   browser.

   .. image:: images/link-external-example.*
      :align: center
      :width: 90%
      :alt: An example of linking to an external digital object

6. Click the "Create" button in the :term:`button block`. When you return to the
   :term:`view page`, the :term:`reference display copy` will be displayed in
   the digital object field, above the other fields linked to that
   :term:`archival description`.

   .. NOTE::

      Users can view or play the :term:`reference display copy` (depending on
      the type of digital object). Authenticated (i.e. logged-in) users can also
      download the :term:`master digital object`.

7. Objects with multiple pages, such as multi-page TIFFs or PDF files, will by
   default be displayed with single-page reference display copies. To have them
   viewed with a pager to allow the user to browse through the pages, go to
   **Admin > Settings > Global > Upload multi-page files as multiple
   descriptions** and select "Yes"; this will also cause all pages of a multi-
   page object to appear individually as child records of the description to
   which the object was uploaded. (See: :ref:`settings <upload-multi-files>`).

.. TIP::

   If you are comfortable with users accessing the
   :term:`master digital object` (e.g. the original full-resolution upload)
   for viewing multi-page files such as PDFs in their browser, you can change
   the default permissions to grant anonymous users (e.g. unauthenticated, or
   not logged in) access to the master via **Admin > Groups** - select the
   "anonymous" group, edit the archival description permissions, and change
   the "Access master" field to "Grant". Users will then be able to click on
   the :term:`reference display copy` to view the original upload. For more
   information, see: :ref:`edit-user-permissions`.


You can upload any file format, but only supported formats can be viewed or
played directly in AtoM. For a list of formats, see
:ref:`File formats <file-formats>`. Formats that are not supported can still be
uploaded: clicking the object will download it to the user's desktop where
(assuming the user has the required software) it can be viewed or played.

See :ref:`below <edit-digital-object>` for more information on making changes to
your :term:`digital object`.

:ref:`Back to top <upload-digital-object>`

.. _upload-multiple-objects:

Upload multiple digital objects
===============================

In AtoM, there is a 1:1 relationship between
:term:`archival descriptions <archival description>` and
:term:`digital objects <digital object>` - that is, only one digital object
may be associated with an archival description, and all digital objects
require an associated description. However, to enable a rapid workflow where
users can upload multiple digital objects without first having to create
associated descriptions, AtoM includes an option to upload multiple digital
objects at once, as :term:`children <child record>` of a selected archival
description. Users can choose what :term:`level of description` is used when
the placeholder descriptions are created; a title can also be added to each
uploaded digital object, which will then be used as the title for the related
description.

.. image:: images/upload-multiple-images.*
   :align: center
   :width: 70%
   :alt: A image of the upload multiple images edit page

.. NOTE::

   The following workflow has been known to fail when using Firefox as your
   webbrowser. For this particular workflow, we recommend using another
   browser, such as Chrome.

**To upload multiple digital objects in AtoM:**

1. Navigate to the :term:`view page` of an existing
   :term:`archival description` in AtoM. You can do this by
   :ref:`browsing <browse>` or by :ref:`searching <search-atom>` for a specific
   archival description - see :ref:`Access content <access-content>` for more
   information on navigation in AtoM.
2. Click on the "More" button in the :term:`button block`; from the menu that
   appears, select "Import digital objects".

.. image:: images/import-digi-objects.*
   :align: center
   :width: 80%
   :alt: An image of the options in the More button located in the button block

3. Select a title for the objects  - this will be used as the title for the
   associated :term:`archival description` that will be created for each object
   uploaded. Each object will also have its own title field once selected, but
   if you do not wish to individually name each object, an automated
   title can be added to all objects using the title field at the top of the
   upload page. Currently the default is image 01, image 02, etc. (which will
   appear as a placeholder (i.e. image %dd%) in the "Title field").

.. image:: images/import-objects-title.*
   :align: center
   :width: 80%
   :alt: Choosing the default title added to child descriptions

4. Choose a :term:`level of description`. Unlike the
   :ref:`link-digital-object` option, which attaches the :term:`digital object`
   directly to the :term:`archival description` at that level, the "Import
   multiple objects" option requires the user to designate a level of
   description (e.g.: Fonds, Subfonds, Collection, Series, Subseries, File,
   Item, Record group, Part, etc). This level of description will be used for
   the new :term:`children <child record>` that are generated as part of the
   upload.

.. image:: images/import-objects-select.*
   :align: center
   :width: 80%
   :alt: Selecting a level of description for the child descriptions

.. TIP::

   For users wishing to include multiple individual images as "views" of a
   single item, AtoM now includes "Part" as a level of description included at
   installation.

5. Click the blue "Select files" link and select multiple files to upload.
6. Once selected, the page will show previews of all the objects. If you like,
   you can edit the title for each object under to the preview. Remember, the
   title you enter here will be the title used for the associated
   :term:`archival description` that will be created for each
   :term:`digital object` uploaded.

.. image:: images/import-objects-title2.*
   :align: center
   :width: 80%
   :alt: Customizing individual description titles for each object uploaded

7. You can quit the upload process at any time by clicking the "Cancel" button
   in the :term:`button block`; any digital objects already uploaded will not be
   saved. Note that simply navigating away from the page by any other means,
   **without first clicking "Import"** will also result in no new digital
   objects being uploaded.
8. Click the "Import" button in the :term:`button block` when you are satisfied
   with your changes. When you return to the :term:`view page`, you will see
   that the objects have all been attached to the :term:`archival description`
   as :term:`child records <child record>` of that description. If the digital
   object :ref:`recurring-carousel` is enabled (see
   :ref:`default-page-elements` for instructions on enabling or disabling the
   carousel), you will also see the thumbnails of your uploaded digital
   objects in the carousel.

.. image:: images/import-objects-children.*
   :align: center
   :width: 80%
   :alt: An image of a description after uploading multiple digital objects

:ref:`Back to top <upload-digital-object>`

.. _upload-pdf:

Upload PDF
==========

A user can link a single PDF and import multiple PDFs into AtoM. A full-text
search of the content of the PDF is available through the main search box. PDFs
that have a text layer will work, including all OCR PDFs and born-digital PDFs
that include a text layer (e.g., exported Word documents) will work. Search
results will refer users to the PDF that contains the search term(s), but will
not reveal the location of the term(s) within the PDF.

Currently, AtoM 2.x truncates PDF text after the first 65,535 bytes.

As mentioned above, it is possible to upload multi-page TIFFs or PDF files to
be displayed with a page viewer and to upload each page as a child object of
the parent. To enable this feature, see :ref:`settings <upload-multi-files>`.

Otherwise, the process for uploading PDFs is the same as described above.


:ref:`Back to top <upload-digital-object>`

.. _edit-digital-object:

Edit digital objects
====================

Any :term:`digital object` that has been uploaded and linked to an
:term:`archival description` can be edited at any time by an authenticated
(i.e. logged-in) user. To do this:

.. |pencil| image:: images/pencil.png
   :height: 18
   :width: 18

1. Navigate to the :term:`view page` of an existing :term:`archival
   description` that has an existing :term:`digital object`.
2. Click on the "More" button in the :term:`button block`; from the menu that
   appears, select "Edit digital object".
3. You will be redirected to the digital object's :term:`edit page`. On this
   page, all representations (i.e. :term:`master <master digital object>`
   representation, :term:`reference <reference display copy>` representation and
   :term:`thumbnail` representation) of the :term:`digital object` will be
   listed, along with information on their Filename, Filesize and Media Type.
4. The Media type is used by the Media type facet in the search/browse pages -
   in some cases, AtoM might not properly detect the media type, and you can
   adjust it here for better results. Values include: Audio, Image, Video,
   Text, and Other. For more information on filter facets in AtoM, see:
   :ref:`recurring-facet-filters`.

Edit reference and thumbnail representations
--------------------------------------------

5. If you wish to use a different image as the :term:`thumbnail` or
   :term:`reference <reference display copy>` version this is also performed
   from the Edit digital object screen. First click delete in Reference
   representation or Thumbnail area.

.. image:: images/edit-thumbnail.*
   :align: center
   :width: 70%
   :alt: Deleting a thumbnail or reference image

6. AtoM will ask the user to confirm that they would like to delete the
   thumbnail/reference image. After confirming, the Edit digital object
   screen will allow the user to upload a new reference representation by
   clicking Browse and selecting a file from their computer, or auto-generate a
   new representation from the master image.

.. image:: images/upload-thumbnail.*
   :align: center
   :width: 70%
   :alt: Upload or create a new thumbnail or reference image.

Save changes
------------

7. You can quit the edit process at any time by clicking the "Cancel" button
   in the :term:`button block`; any edits made to digital objects will not be
   saved. Note that simply navigating away from the page by any other means,
   **without first clicking "Save"** will also result in no new digital objects
   being uploaded.

8. Once all your changes have been made, click the "Save" button in the
   :term:`button block`. You will be redirected back to the
   :term:`archival description's <archival description>` :term:`view page`.

All changes made can be edited once again, at any time, by following the steps
outlined above.

:ref:`Back to top <upload-digital-object>`

.. _rename-digital-object:

Edit the filename of a linked digital object
============================================

For locally uploaded digital objects, you can edit the file name of the
digital object after it has already been uploaded, using the "Rename" module.
Once edited, AtoM will automatically update all related file paths to ensure
that the link between the digital object and the associated
:term:`archival description` is maintained.

.. IMPORTANT::

   This feature is best used for **locally** uploaded digital objects, **not**
   digital objects linked via URL to an external location, such as the web.

   Technically the feature will work with external links, but all you are
   renaming in AtoM is the filename stored in the database associated with the
   :term:`master digital object`, and the filenames of any locally generated
   derivatives such as the :term:`reference display copy` and the
   :term:`thumbnail`. When linking a digital object in AtoM via URL, the
   master is not stored in AtoM, but local derivatives are created for use in
   search/browse results and the :term:`view page` of the linked description.
   For more on linking digital objects in AtoM, see above:
   :ref:`link-digital-object`. If you do edit the filename of an external
   linked digital object, AtoM will store the filename locally, and use it to
   update the filenames of the derivatives - but the external object will not
   be affected, and the link displayed in the digital object metadata area
   will be unchanged.

The Rename module used to edit the linked digital object filename can also be
used to edit the title of the associated :term:`archival description`, and its
:term:`slug` - detailed instructions on how to use it for these other purposes
are included on the :ref:`archival-descriptions` documentation page - see:
:ref:`rename-title-slug`.

**To change the filename of a linked digital object:**

1. Navigate to the :term:`view page` of an existing
   :term:`archival description` with a linked digital object in AtoM. You can
   do this by :ref:`browsing <browse>` or by :ref:`searching <search-atom>`
   for a specific  archival description - see :ref:`access-content` for more
   information on navigation in AtoM.
2. Scroll down to the :term:`button block` at the bottom of the page, and
   click on the "More" button - a menu will open with further options. Click
   on "Rename" to open the Rename module.

.. image:: images/rename-button.*
   :align: center
   :width: 80%
   :alt: An image of the More button menu opened on an archival description

3. AtoM will redirect you to the Rename module page. You will see 3
   :term:`fields <field>` - one for the title of the description, one for
   the slug; the third field is for the filename of the digital object
   linked to the description.

.. image:: images/rename-page.*
   :align: center
   :width: 80%
   :alt: An image of the Rename module's available fields

.. SEEALSO::

   For more information on editing the :term:`slug` and/or title of a
   description with the rename module, see: :ref:`rename-title-slug`.

4. To the right of the edit fields, there is a checkbox corresponding to each
   field. By default, the title and slug checkboxes will be checked, and the
   filename field will be unchecked. The checkbox associated with a field must
   be checked to enable editing. You can uncheck these fields at any time to
   disable them - doing so will undo any changes made and prevent the field from
   updating when the "Update" button is clicked. To edit the filename of the
   linked :term:`digital object`, check the "Update filename" box. You also
   might wish to uncheck the Title and Slug boxes, to prevent any accidental
   edits.

5. Place your cursor in the filename :term:`field` and make changes as necessary.
   For reference, the original value before  your changes is displayed below
   the field.

.. image:: images/rename-filename.*
   :align: center
   :width: 80%
   :alt: An image of the filename being edited in the Rename module

.. IMPORTANT::

   AtoM will automatically sanitize a filename you submit, including:

   * Replacing spaces with hyphens
   * Stripping uppercase characters to lower
   * Removing special characters (e.g. ! @ # $ % ^ & etc)
   * Removing stopwords (e.g. a, an, the, etc)

   This is similar to how a :term:`slug` is sanitized - for more information,
   see: :ref:`slugs-in-atom`.

   **However**, unlike when editing a slug (see :ref:`rename-title-slug`),
   AtoM will **not** give you any warning or notification when making these
   changes after you submit the new filename. You will have to look at the
   digital object metadata area to review the sanitized filename, and repeat
   the above steps if needed.

   We recommend using lowercase alphanumeric characters with no spaces or
   stopwords when choosing your new filename.

6. If you do **not** wish to save your changes, you can click the "Cancel"
   button in the :term:`button block` at the bottom of the Rename module page.
   Note that navigating away from the Rename page will also result in no changes
   being saved.

7. When you are finished making your edits, save your changes by clicking the
   "Update" button located in the :term:`button block` at the bottom of the
   Rename module page. AtoM will redirect you to the :term:`view page` for the
   related :term:`archival description`. A notification banner at the top of
   the page will let you know that the description has been updated.

.. image:: images/rename-notification.*
   :align: center
   :width: 80%
   :alt: An image of the notification banner after a successful rename

8. You can see the updated filename in the Digital object metadata
   :term:`area <information area>` at the bottom  of the record. If you are
   unhappy with the results, you can repeat steps 1-7 as necessary.

.. image:: images/object-metadata-area.*
   :align: center
   :width: 80%
   :alt: An image of the digital object metadata area on an archival description

:ref:`Back to top <upload-digital-object>`

.. _delete-digital-object:

Delete digital objects
======================

To delete a :term:`digital object` that has been uploaded and linked to an
:term:`archival description`:

1. Navigate to the :term:`view page` of an existing :term:`archival
   description` that has an existing :term:`digital object`.
2. Click on the "More" button in the :term:`button block`; from the menu that
   appears, select "Edit digital object". You will be redirected to the digital
   object's :term:`edit page`.
3. Scroll to the bottom of the page and click "Delete". You will be prompted to
   confirm that you wish to "Delete" the digital object; click "Delete" once
   again. You will be redirected to the archival description's
   :term:`view page`.

:ref:`Back to top <upload-digital-object>`

.. _digital-object-storage:

Digital object storage
======================

In AtoM, administrators can track digital object storage per :term:`repository`.
Storage limits may be placed on individual repositories by in-house server
capacity or on hosted server agreements.

If you are utilizing a multi-institutional / portal instance of AtoM, you will
need to check with the site administrator to learn the digital object storage
limitations.

For more information, see :ref:`Managing digital object storage
<manage-digital-object-storage>`.

.. _file-formats:

Files formats
=============

A number of file formats are supported as digital objects in AtoM. Files in
other formats can still be uploaded to AtoM; they just cannot be directly
accessed or streamed within AtoM itself. In these cases the user must
download the file from AtoM to his or her desktop and (assuming the user
has the requisite software) access the content there.

The table below shows image, audio and video formats which can be viewed in
AtoM:

+----------------+--------------------------------+--------------------------+
| Image          | Audio                          | Video                    |
+================+================================+==========================+
| PDF            | 8SVX                           | AVS                      |
+----------------+--------------------------------+--------------------------+
| BMP            |  AC-3                          | BFI                      |
+----------------+--------------------------------+--------------------------+
| GIF            | Apple Lossless                 | CamStudio CSCD           |
+----------------+--------------------------------+--------------------------+
| PNG            | ATRAC3                         | Cinepak                  |
+----------------+--------------------------------+--------------------------+
| JPEG           | Cook Codec                     | Creative YUV (CYUV)      |
+----------------+--------------------------------+--------------------------+
| V.Flash PTX    | EA ADPCM                       | DNxHD                    |
+----------------+--------------------------------+--------------------------+
| SGI            | FLAC                           | Flash Screen Video       |
+----------------+--------------------------------+--------------------------+
| Sun Rasterfile | Intel Music Coder              | FFV1                     |
+----------------+--------------------------------+--------------------------+
| FLIC           | Monkey's Audio                 | H.261                    |
+----------------+--------------------------------+--------------------------+
| TIFF           | MP2                            | H.263                    |
+----------------+--------------------------------+--------------------------+
| PNM            | MP3                            | H.264/MPEG-4 AVC         |
+----------------+--------------------------------+--------------------------+
|                | Nellymoser Asao Codec in Flash | Huffyuv                  |
+----------------+--------------------------------+--------------------------+
|                | QDM2                           | id Software RoQ Video    |
+----------------+--------------------------------+--------------------------+
|                | RealAudio 1.0                  | Intel Indeo 2            |
+----------------+--------------------------------+--------------------------+
|                | RealAudio 2.0                  | Intel Indeo 3            |
+----------------+--------------------------------+--------------------------+
|                | Shorten                        | LOCO                     |
+----------------+--------------------------------+--------------------------+
|                | Truespeech                     | Mimic[3]                 |
+----------------+--------------------------------+--------------------------+
|                | TTA                            | MJPEG                    |
+----------------+--------------------------------+--------------------------+
|                | TXD                            | MPEG-4 Part 2            |
+----------------+--------------------------------+--------------------------+
|                | Vorbis                         | Apple Computer QuickDraw |
+----------------+--------------------------------+--------------------------+
|                | WavPack                        | Quicktime Graphisc SMC   |
+----------------+--------------------------------+--------------------------+
|                | Windows Media Audio 1          | RealVideo RV10           |
+----------------+--------------------------------+--------------------------+
|                | Windows Media Audio 2          | RL2                      |
+----------------+--------------------------------+--------------------------+
|                |                                | Smacker video            |
+----------------+--------------------------------+--------------------------+
|                |                                | Snow                     |
+----------------+--------------------------------+--------------------------+
|                |                                | Sorenson SVQ1            |
+----------------+--------------------------------+--------------------------+
|                |                                | Sorenson SVQ3            |
+----------------+--------------------------------+--------------------------+
|                |                                | Theora                   |
+----------------+--------------------------------+--------------------------+
|                |                                | Asus V1                  |
+----------------+--------------------------------+--------------------------+
|                |                                | Asus V2                  |
+----------------+--------------------------------+--------------------------+
|                |                                | VMware VMnc              |
+----------------+--------------------------------+--------------------------+
|                |                                | On2 VP3                  |
+----------------+--------------------------------+--------------------------+
|                |                                | On2 VP5                  |
+----------------+--------------------------------+--------------------------+
|                |                                | On2 VP6                  |
+----------------+--------------------------------+--------------------------+
|                |                                | Westwood Studios VQA     |
+----------------+--------------------------------+--------------------------+
|                |                                | Microsoft WMV            |
|                |                                | v 7, 8 and 9             |
+----------------+--------------------------------+--------------------------+
|                |                                | Wing Commander/Xan Video |
+----------------+--------------------------------+--------------------------+

.. note::

   AtoM uses FFmpeg to handle audio-visual files. The table above shows
   the file formats supported by FFmpeg.

:ref:`Back to top <upload-digital-object>`
