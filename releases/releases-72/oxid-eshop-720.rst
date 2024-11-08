OXID eShop 7.2.0
================

Release-Datum: tbd

Änderungen im Überblick
-----------------------
Übersetze:
* Core: Veraltete Demodaten-Bilder aus der CE Komponente entfernt
* Core: Support von PHP 8.2/8.3
* Core: Support von MySQL 8.0 und MariaDB11
* Core: Order mail disable via parameter
* Core: Verbesserung der Password-Vergessen/Passwort-Änderungs Funktionalität.

* APEX: flexible Zoompics (feature)
* APEX: script in ajax call (feature)
* APEX: Google Analytics 4 (Pageaccess, orders)
* APEX: SEO Microdata Update

* GDPR user data export in admin

* VCMS Bundle migration to new layout, improvements siehe changelogs


Korrekturen
-----------

* Die Compilation 7.2.0 beinhaltet die Korrekturen aus Compilation 7.0.4/7.1.1:
  - Netto-Preise im Frontend
  - Optimierte ShopId-Berechnung

* User registration in the Private Sales mode - Emailbestätigung zur Aktivierung ist zwingend benötigt

* New item in basket message display `#0007548 <https://bugs.oxid-esales.com/view.php?id=7548>`_, `PR-964 <https://github.com/OXID-eSales/oxideshop_ce/pull/964>`_

* Multiple language creation `#0007683 <https://bugs.oxid-esales.com/view.php?id=7683>`_

* Twig Component ifcontent extension `#0007231 <https://bugs.oxid-esales.com/view.php?id=7231>`_

* Visual CMS 7.0.1 enthält die Korrekturen aus Visual CMS 4.1.1/6.0.1

* APEX siehe changelog



En Detail
=========

User Experience
---------------

Verbessern Sie mit drei neuen Zoom-Optionen das Einkaufserlebnis für Ihre Kunden in Ihrem OXID eShop.

* Hover Zoom: Diese Funktion bietet eine interaktive Möglichkeit, Produktbilder im Detail zu betrachten.

  Wenn der Mauszeiger über das Bild fährt, wird es vergrößert, und die Vergrößerung folgt der Mausbewegung.

  Dies erlaubt es den Nutzern, verschiedene Bildbereiche genau zu untersuchen und erhöht die Interaktivität und das Engagement.

* Modal-Zoom: Beim Klick auf das Produktbild wird dieses in einem größeren Modal-Fenster geöffnet, in dem weitere Details sichtbar werden.

  Zusätzlich kann der Nutzer innerhalb des Modals in das Bild hineinzoomen, um besonders feine Details zu erkennen.

  Dies bietet eine umfassende Möglichkeit, Produkte genau unter die Lupe zu nehmen.

* Magnifier-Zoom: Hier wird eine Lupenfunktion aktiviert, wenn der Mauszeiger über das Bild fährt.

  Ein separater Bereich zeigt eine stark vergrößerte Ansicht des Bildausschnitts direkt unter dem Mauszeiger.

  Dies ermöglicht eine präzise Betrachtung spezifischer Produktdetails, ohne das gesamte Bild zu vergrößern.


Sie können den gewünschten Zoom global für Ihren OXID eShop einstellen. Zusätzlich können Sie für einzelne Artikel eine individuelle Zoom-Art festlegen.

Weitere Informationen finden Sie unter :ref:`konfiguration/bilder:Zoom wählen`.


Die Änderungen im Überblick
---------------------------

* Sicherheit & Zuverlässigkeit

    Aus Sicherheitsgründen erfordert OXID eShop 7.2.0 die Composer-Version 2.7.7
    Weitere Informationen finden Sie unter
    * `Composer Version 2.7.7 <https://github.com/composer/composer/releases/tag/2.7.7>`_
    * `CVE-2024-35241 <https://github.com/advisories/GHSA-47f6-5gq3-vx9c>`_
    * `CVE-2024-35242 <https://github.com/advisories/GHSA-v9qv-c7wm-wgmf>`_

   Verbesserung der Password-Vergessen/Passwort-Änderungs Funktionalität.


* Barrierefreiheit
  Kleinere Verbesserungen im APEX-Theme, siehe Changelog


* Visual CMS & Mediathek
  Siehe Changelog

* Neue Funktionen für Entwickler

  Bestellbestätigungsemaio kann per Parameter ausgeschaltet werden:
  https://github.com/OXID-eSales/developer_documentation/blob/b-7.2.x/development/modules_components_themes/project/parameters.rst

  APEX: Javascript execution on ajax call, am besten auf Doku verlinken


Verbesserung im Shop-Administrationsbereich
-------------------------------------------

Newsletter
^^^^^^^^^^
.. todo: OXDEV-7028: Newsletter export data enhanced · OXID-eSales/oxideshop-user-documentation@a19e24b -- keine neue Funktion, nur Doku erweitert: betrieb/newsletter/newsletter.rst

As a shop owner I want to know exactly what Export users function does: https://oxid-esales.atlassian.net/browse/OXDEV-7028

Statt

Die Datensätze werden in eine CSV-Datei geschrieben, deren Dateinamen aus :file:`Export_recipients_`, einem angehängten Datum im Format JJJJ-MM-TT und der Dateiendung :file:`.csv` besteht. Die Datei enthält Anrede, Vorname, Nachname, E-Mail-Adresse, Opt-in-Status und zugeordnete Benutzergruppen für jeden Abonnenten. Opt-in-Status kann abonniert, nicht abonniert oder nicht bestätigt sein. Die Datei kann direkt im verwendeten Browser geöffnet oder lokal auf dem Rechner gespeichert werden.
Die Datensätze werden in eine CSV-Datei geschrieben, deren Dateinamen aus :file:`Export_user_recipient_status_`, einem angehängten Datum im Format JJJJ-MM-TT und der Dateiendung :file:`.csv` besteht. Die Datei enthält Anrede, Vorname, Nachname, E-Mail-Adresse, Opt-in-Status, Land und zugeordnete Benutzergruppen für jeden Abonnenten. Opt-in-Status kann abonniert, nicht abonniert oder nicht bestätigt sein. Die Datei kann direkt im verwendeten Browser geöffnet oder lokal auf dem Rechner gespeichert werden.

:ref:`betrieb/newsletter/newsletter:Newsletter`


Make mail sending optional (configuration option)
^^^^^^^^^^^^^^^^^^^^^^^^^^

New parameter oxid_esales.email.disable_order_emails to enable and disable sending order emails

.. todo: https://oxid-esales.atlassian.net/browse/OXDEV-6846
.. todo: https://github.com/OXID-eSales/developer_documentation/commit/5c970ea708e2f2b9dd67a2cfcd0129acb5df9c1a

.. todo: Ref testen: https://docs.oxid-esales.com/developer/en/latest/development/modules_components_themes/project/parameters.html`_




Neue Funktionen für Entwickler
------------------------------

Systemvoraussetzungen
^^^^^^^^^^^^^^^^^^^^^

* MySQL 8.0 (MySQL 5.7 wird unterstützt, aber wir empfehlen es sicht)
* MariaDB (getestet mit MariaDB 11)
* PHP Versionen 8.2 oder 8.3



Sicherheit & Zuverlässigkeit
----------------------------


Barrierefreiheit
----------------



Visual CMS & Mediathek
----------------------

.. todo: Input MF

Weitere Informationen zu Änderungen finden Sie in den folgenden Changelogs:

* Visual CMS: https://github.com/OXID-eSales/visual_cms_module/blob/v7.0.1/CHANGELOG-7.x.md
* WYSIWYG-Editor: https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md
* Mediathek: https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md

Verbesserung im Shop-Administrationsbereich
-------------------------------------------




Neue Funktionen für Entwickler
------------------------------

Abhängigkeiten zwischen Modulen definieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#tbd


Verbesserung im Shop-Administrationsbereich
-------------------------------------------

tbd

Neue Funktionen für Entwickler
------------------------------


Clean Up
--------



Aktualisierte Komponenten
^^^^^^^^^^^^^^^^^^^^^^^^^

Wir haben die folgenden Komponenten und Module aktualisiert:

* `OXID eShop CE (Update von v7.1.0 auf v7.2.0) <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE (Update von v7.1.0 auf v7.2.0)
* OXID eShop EE (Update von v7.1.0 auf v7.2.0)
* `Apex theme (Update von v1.4.0 auf v2.0.0) <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md#v200---2024-10-14>`_
* `Twig admin theme (Update von v2.4.0 auf v2.5.0) <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE (Update von v2.4.0 auf v2.5.0) <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE (Update von v2.4.0 auf v2.5.0)
* Twig component EE (Update von v2.4.0 auf v2.5.0)
* `OXID eShop demo data CE (Update von v8.0.1 auf v8.0.2) <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.1/CHANGELOG.md>`_
* OXID eShop demo data PE (update from v8.0.1 to v8.0.2)
* OXID eShop demo data EE (Update von v8.0.2 auf v8.0.3)
* `OXID eShop Demodata Installer (Update von 3.2.0 auf 3.3.0) <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_
* `OXID eShop doctrine migration integration (Update von v5.2.0 auf v5.3.0) <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `WYSIWYG Editor + Mediathek (Update von v4.1.0 auf v4.2.0) <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `GDPR opt-in (Update von v4.0.0 auf v4.1.0) <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md#v410---2024-10-14>`_
* `Media Library Module (Update von v2.0.0 auf v2.1.1) <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* Visual CMS (Update von v6.0.0 auf v7.0.2)

Komponenten der Compilation
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Compilation enthält die folgenden Komponenten:

* `OXID eShop CE 7.2.0 <https://github.com/OXID-eSales/oxideshop_ce/blob/v7.2.0/CHANGELOG-7.2.md>`_
* OXID eShop PE 7.2.0
* OXID eShop EE 7.2.0

* `Apex theme 2.0.0 <https://github.com/OXID-eSales/apex-theme/blob/v2.0.0/CHANGELOG-2.x.md>`_

* `Twig admin theme 2.5.0 <https://github.com/OXID-eSales/twig-admin-theme/blob/v2.5.0/CHANGELOG-2.x.md>`_
* `Twig component CE 2.5.0 <https://github.com/OXID-eSales/twig-component/blob/v2.5.0/CHANGELOG-2.x.md>`_
* Twig component PE 2.5.0
* Twig component EE 2.5.0

* `OXID eShop composer plugin 7.2.0 <https://github.com/OXID-eSales/oxideshop_composer_plugin/blob/v7.2.0/CHANGELOG-7.x.md>`_
* `OXID eShop Views Generator 2.2.0 <https://github.com/OXID-eSales/oxideshop-db-views-generator/blob/v2.2.0/CHANGELOG.md>`_
* `OXID eShop demo data installer 3.3.0 <https://github.com/OXID-eSales/oxideshop-demodata-installer/blob/v3.3.0/CHANGELOG-3.x.md>`_

* `OXID eShop demo data CE 8.0.2 <https://github.com/OXID-eSales/oxideshop_demodata_ce/blob/v8.0.2/CHANGELOG.md>`_
* OXID eShop demo data PE 8.0.2
* OXID eShop demo data EE 8.0.3

* `OXID eShop doctrine migration integration 5.3.0 <https://github.com/OXID-eSales/oxideshop-doctrine-migration-wrapper/blob/v5.3.0/CHANGELOG-5.x.md>`_
* `OXID eShop facts 4.2.0 <https://github.com/OXID-eSales/oxideshop-facts/blob/v4.2.0/CHANGELOG-4.x.md>`_
* `Unified Namespace Generator 5.1.0 <https://github.com/OXID-eSales/oxideshop-unified-namespace-generator/blob/v5.1.0/CHANGELOG.md>`_

* `GDPR Opt-In 4.1.0 <https://github.com/OXID-eSales/gdpr-optin-module/blob/v4.1.0/CHANGELOG.md>`_
* `OXID Cookie Management powered by usercentrics 3.0.0 <https://github.com/OXID-eSales/usercentrics/blob/v3.0.0/CHANGELOG.md>`_
* Visual CMS 7.0.2 (PE/EE)

* `WYSIWYG Editor 4.2.0 <https://github.com/OXID-eSales/ddoe-wysiwyg-editor-module/blob/v4.2.0/CHANGELOG.md>`_
* `Mediathek 2.1.1 <https://github.com/OXID-eSales/media-library-module/blob/v2.1.1/CHANGELOG.md>`_
* `Makaira 2.1.2 <https://github.com/MakairaIO/oxid-connect-essential/blob/2.1.2/CHANGELOG.md>`_
* `Eye-Able 3.0.3 <https://github.com/Tobias-Eye-Able/eye-able-oxid-module/blob/v3.0.3/CHANGELOG.md>`_


Korrekturen
-----------

Die Korrekturen finden Sie im `Changelog <https://github.com/OXID-eSales/oxideshop_ce/blob/b-7.2.x/CHANGELOG-7.2.md>`_.

Installation
------------

Zum Installieren oder Aktualisieren folgen Sie den Anleitungen unter :doc:`Installation <../../installation/index>`.


.. Intern: , Status:
