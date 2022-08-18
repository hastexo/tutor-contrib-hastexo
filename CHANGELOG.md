Unreleased
-----------------------------

* [BREAKING CHANGE] Support Tutor 14 and Open edX Nutmeg. This entails
  a configuration format change from JSON to YAML, meaning that from
  version 1.0.0 this plugin only supports Tutor versions from 14.0.0
  (and with that, only Open edX versions from Nutmeg).

* BREAKING CHANGE: Update the `ASGI_APPLICATION` definition and
   add `LMS_HOST` to `ALLOWED_HOSTS` to support running the 
   `hastexo_guacamole_client` with Channels 3.

Version 0.3.0 (2022-06-29)
-----------------------------
* Use Tutor v1 plugin API


Version 0.2.0 (2022-06-28)
-----------------------------
* Add `HASTEXO_ENABLE_SUSPENDER` and `HASTEXO_ENABLE_REAPER` to
  effectively enable/disable the `suspender` and `reaper` deployments
  (by setting their respective replica counts to 1 or 0).
* Add an option to scale the number of instances via
  `HASTEXO_REPLICA_COUNT` setting.

Version 0.1.0 (2022-04-20)
-----------------------------

* Refactor the way we add `HASTEXO_XBLOCK_SETTINGS` to the
  `XBLOCK_SETTINGS`. Add the settings under the `hastexo` key
  without overriding the general definition.
* Fix terminal customisation options. Override the default
  settings module for the `hastexo_guacamole_client`
  so that the `XBLOCK_SETTINGS` will be present in the
  `hastexo` container and thus, will make it possible to
  define custom settings for the terminal window.
* Add support for installing custom fonts for terminal.
  The required font will have to be installed in the
  `guacd` container. Add an option to build a custom
  `guacd` image while keeping the option of using the
  upstream base image in case a custom font is not needed.

## Version 0.0.2 (2022-02-25)

* Fix version number as it appears in pip list (previously, all
  installations would show up as version 0.0.0, including
  installations from the 0.0.1 tag).


## Version 0.0.1 (2022-02-24)

**Experimental. Do not use in production.**

* Add basic testing via tox
* Initial Git import
