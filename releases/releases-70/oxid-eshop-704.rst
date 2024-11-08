OXID eShop 7.0.4
================

Release-Datum: xx.xx.2024

Changes
-------

To close a security vulnerability in Composer, install OXID eShop 7.0.4.

For security reasons, OXID eShop 7.0.4 requires Composer version 2.7.7

For more information, see

* `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
* `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
* `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_

Corrections
-----------

* Display of net prices in the frontend

  For net prices, in the frontend, it could happen that a placeholder was displayed instead of 0% VAT.

* Performance improvement: ``ShopId`` calculation only once per request

  Under certain circumstances, the ``ShopId`` was calculated several times during a request.

  Solution: ``ShopId`` is stored in the context object as a private property.

  Advantage: This optimization leads to an acceleration of your OXID eShop.

  We recommend that all shop owners implement this update in order to benefit from the performance improvements.

* Visual CMS: (Professional and Enterprise Edition only): Automatic migration to new layout classes.

New features and optimizations in detail
----------------------------------------

For more information about changes to the compilation in the metapackage, see `<https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.0.3...v7.0.4>`_.

For more information about corrections, see the `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.5/CHANGELOG-7.0.md>`_.

Updated components
^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* `OXID eShop CE (update from 7.0.4 to 7.0.5) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.5/CHANGELOG-7.0.md>`_
* `Visual CMS (update from 4.0.2 to 4.1.1) <https://github.com/OXID-eSales/visual_cms_module/blob/v4.1.1/CHANGELOG-4.x.md>`_


Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components:

* `OXID eShop CE 7.0.5 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.0.5/CHANGELOG-7.0.md>`_
* `OXID eShop PE 7.0.0 <https://github.com/OXID-eSales/oxideshop_pe/blob/v7.0.0/CHANGELOG.md>`_
* `OXID eShop EE 7.0.1 <https://github.com/OXID-eSales/oxideshop_ee/blob/v7.0.1/CHANGELOG-7.0.md>`_
* `Apex theme 1.2.2 <https://github.com/OXID-eSales/apex-theme/blob/v1.2.2/CHANGELOG-1.x.md>`_
* `Twig admin theme 2.3.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.3.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.3.0 <https://github.com/OXID-eSales/twig-component/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component PE 2.3.0 <https://github.com/OXID-eSales/twig-component-pe/blob/v2.3.0/CHANGELOG.md>`_
* `Twig component EE 2.3.0 <https://github.com/OXID-eSales/twig-component-ee/blob/v2.3.0/CHANGELOG.md>`_

* `OXID eShop composer plugin 7.1.1 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.1.1/CHANGELOG.md>`_
* `OXID eShop Views Generator 2.1.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.1.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.1.1 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.1.1/CHANGELOG.md>`_
* `OXID eShop demo data CE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop demo data PE 8.0.0 <https://github.com/OXID-eSales/oxideshop_demodata_pe/blob/v8.0.0/CHANGELOG.md>`_
* `OXID eShop demo data EE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ee/blob/v8.0.1/CHANGELOG.md>`_
* `OXID eShop doctrine migration integration 5.1.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.1.0/CHANGELOG.md>`_
* `OXID eShop facts 4.1.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.1.0/CHANGELOG.md>`_
* `Unified Namespace Generator 4.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v4.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 3.0.1 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v3.0.1/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 2.0.2 <https://github.com/OXID-eSales/usercentrics/blob/v2.0.2/CHANGELOG.md>`_
* `Visual CMS 4.1.1 <https://github.com/OXID-eSales/visual_cms_module/blob/v4.1.1/CHANGELOG-4.x.md>`_ (PE/EE)
* `WYSIWYG Editor + Media Library 3.0.2 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v3.0.2/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_

Installation
------------

To install or update, follow the instructions under :ref:`installation/index:Installation`.

.. Intern: , Status:
