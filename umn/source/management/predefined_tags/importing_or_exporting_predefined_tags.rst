:original_name: en-us_topic_0056266555.html

.. _en-us_topic_0056266555:

Importing or Exporting Predefined Tags
======================================

Importing Predefined Tags
-------------------------

If you have inventory tags, you can quickly import them to the TMS predefined tags to facilitate subsequent resource association.

The predefined tag import function allows you to import the .csv file exported from a third party to TMS. The encoding format of the .csv file must be UTF-8.

If duplicate content exists between the current environment and the imported file, the content of the current environment will be overwritten after the import.

When editing tags to be imported, pay attention to the following restrictions:

-  Each user can create up to 500 predefined tags.
-  You can enter a maximum of 36 and 43 characters for **Key** and **Value**, respectively. Both **Key** and **Value** can contain only digits, letters, hyphens (-), at signs (@), and underscores (_).

.. important::

   Predefined tag importation does not support .csv files that have been modified in Excel. Attempting to import such files will produce garbled characters and result in an importation failure. To edit a .csv file, open it with notepad.

To import predefined tags, perform the following steps:

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Choose **Predefined Tags**.

#. Click **Download template (CSV file)**.

#. Fill in the template as prompted.

#. Click **Import** and select the target file.

#. Click **OK**.

   The predefined tags are imported successfully and displayed in the predefined tag list.

Exporting Predefined Tags
-------------------------

Tag files or templates downloaded with Internet Explorer 9 cannot be imported into other browsers. Those downloaded with other browsers cannot be imported into Internet Explorer 9.

To export predefined tags for editing, perform the following steps:

#. Log in to the management console.

#. Under **Management & Deployment**, select **Tag Management Service**.

#. Choose **Predefined Tags**.

#. Select the predefined tags you want to export.

#. Click **Export**.

   The system saves the exported .csv file and the predefined tags are exported successfully.
