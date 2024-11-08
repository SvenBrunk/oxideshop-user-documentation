OXID eShop 7.1.1
================

Release date: xx.xx.2024

Security updates
----------------

Composer
^^^^^^^^

Security vulnerability closed: Installation of OXID eShop 7.1.1 required to fix a vulnerability in Composer.

Prerequisite: OXID eShop 7.1.1 requires Composer version 2.7.7 to increase security.

For more information, see

* `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
* `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
* `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_


WYSIWYG-Editor
^^^^^^^^^^^^^^

Improved security: JavaScript in CMS content is no longer executed in the store back office as pre-filtering has been implemented.

Corrections
-----------

* Compilation 7.1.1 contains the corrections from compilation 7.0.4:

  * Frontend: Correct display of net prices
  * Backend: Optimization of performance by improving the `ShopId`` calculation

  For more information, see the `Release Notes for OXID eShop 7.0.4 <https://docs.oxid-esales.com/eshop/en/7.0/releases/releases-70/oxid-eshop-704.html#corrections>`_.

* User groups: PR #962 corrects the return value when deleting user groups. For more information, see `GitHub-PR #962 <https://github.com/OXID-eSales/oxideshop_ce/pull/962>`_.
* Translation files: PR #963 enables loading translation files for custom themes. For more information, see `GitHub-PR #963 <https://github.com/OXID-eSales/oxideshop_ce/pull/963>`_.
* APEX Theme: Various fixes (for more information, see the changelog).
* Media library: Various fixes (for more information, see the changelog).
* VisualCMS (PE/EE only): Automatic migration to new layout classes (for more information, see the changelog).

Find the changelog under `Changelog 7.1.x <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.1.x/CHANGELOG-7.1.md>`_.

Components
-----------

Find the changes to the compilation in the metapackage. For more information, on Github see the comparison of versions `v7.1.0...v7.1.1 <https://github.com/OXID-eSales/oxideshop_metapackage_ce/compare/v7.1.0...v7.1.1>`_.

Updated components
^^^^^^^^^^^^^^^^^^^^^^^^^

We have updated the following components and modules:

* `OXID eShop CE (update from 7.1.0 to 7.1.1) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.1/CHANGELOG-7.1.md>`_
* `WYSIWYG Editor Module (update from 4.0.0 to 4.1.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.1.0/CHANGELOG.md>`_
* `Visual CMS (update from 5.0.1 to 6.0.1) <https://github.com/OXID-eSales/visual_cms_module/blob/v6.0.1/CHANGELOG-6.x.md>`_
* `Eye Able Assist (update from 3.0.1 to 3.0.3) <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_
* `APEX Theme (update from 1.3.0 to 1.4.0) <https://github.com/OXID-eSales/apex-theme/blob/v1.4.0/CHANGELOG.md>`_
* `Media library (update from 1.0.0 to 2.0.1) <https://github.com/OXID-eSales/media-library-module/blob/v2.0.1/CHANGELOG.md>`_
* `Unified Namespace Generator (update from 5.0.0 to 5.1.0) <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_


Components of the compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The compilation contains the following components (updated versions):

* `OXID eShop CE 7.1.1 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.1.1/CHANGELOG-7.1.md>`_
* OXID eShop PE 7.1.0
* OXID eShop EE 7.1.0

* `Apex theme 1.4.0 <https://github.com/OXID-eSales/apex-theme/blob/v1.4.0/CHANGELOG.md>`_

* `Twig admin theme 2.4.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.4.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.4.0 <https://github.com/OXID-eSales/twig-component/blob/v2.4.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.4.0
* Twig component EE 2.4.0

* `OXID eShop composer plugin 7.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.2.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.2.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.1 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.1
* OXID eShop demo data EE 8.0.2

* `OXID eShop doctrine migration integration 5.2.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.2.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.2.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.0.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.0.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 6.0.1 (PE/EE)

* `WYSIWYG Editor 4.1.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.1.0/CHANGELOG.md>`_
* `Mediathek 2.0.1 <https://github.com/OXID-eSales/media-library-module/blob/v2.0.1/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/tree/v3.0.3>`_

Installation
------------

To install or upgrade, follow the instructions under :doc:`Installation <../../installation/index>`.


.. Intern: , Status:
