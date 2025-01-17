:original_name: en-us_topic_0056765935.html

.. _en-us_topic_0056765935:

Creating or Deleting Predefined Tags
====================================

Function
--------

This API is used to create or delete predefined tags. You can add tags to resources using the predefined tags.

This API supports idempotency and batch processing.

.. note::

   Idempotent operations refer to invoking the same API for multiple times by using the same parameters, which have the same impact on the system.

URI
---

POST /v1.0/predefine_tags/action

Request
-------

-  Parameter description

   .. table:: **Table 1** Parameters in the request

      +-----------------+-----------------+------------------------------+-------------------------------------------------------------------------------------------------+
      | Name            | Mandatory       | Type                         | Description                                                                                     |
      +=================+=================+==============================+=================================================================================================+
      | action          | Yes             | String                       | Specifies the operation identifier.                                                             |
      |                 |                 |                              |                                                                                                 |
      |                 |                 |                              | This parameter value is case sensitive and can be **create** or **delete**.                     |
      +-----------------+-----------------+------------------------------+-------------------------------------------------------------------------------------------------+
      | tags            | Yes             | List<predefine_tag_request>  | Specifies the tag list.                                                                         |
      |                 |                 |                              |                                                                                                 |
      |                 |                 |                              | For details, see :ref:`Table 2 <en-us_topic_0056765935__en-us_topic_0056765542_table46817064>`. |
      +-----------------+-----------------+------------------------------+-------------------------------------------------------------------------------------------------+

-  **predefine_tag_re**\ **quest** field description

   .. _en-us_topic_0056765935__en-us_topic_0056765542_table46817064:

   .. table:: **Table 2** Parameter description

      +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Name            | Mandatory       | Type            | Description                                                                                                                                             |
      +=================+=================+=================+=========================================================================================================================================================+
      | key             | Yes             | String          | Specifies the key.                                                                                                                                      |
      |                 |                 |                 |                                                                                                                                                         |
      |                 |                 |                 | It cannot be left blank and can contain a maximum of 36 Unicode characters. Can contain only digits, letters, hyphens (-), and underscores (_).         |
      +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------+
      | value           | Yes             | String          | Specifies the value.                                                                                                                                    |
      |                 |                 |                 |                                                                                                                                                         |
      |                 |                 |                 | Each value contains a maximum of 43 Unicode characters and can be an empty string. Can contain only digits, letters, hyphens (-), and underscores (_).  |
      +-----------------+-----------------+-----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------+

-  Example request

   .. code-block:: text

      POST https://TMS endpoint/v1.0/predefine_tags/action

   .. code-block::

      {
          "action": "create",
          "tags": [
              {
                  "key": "ENV1",
                  "value": "DEV1"
              },
              {
                  "key": "ENV2",
                  "value": "DEV2"
              }
          ]
      }

Response
--------

-  Parameter description

   None

-  Example response

   None

Status Codes
------------

See :ref:`Status Code <en-us_topic_0130578970>`.

Error Codes
-----------

See :ref:`Error Code Description <en-us_topic_0057939857>`.
