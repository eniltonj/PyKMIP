=========
Changelog
=========

.. _v0.8:

0.8 - `master`_
~~~~~~~~~~~~~~~

.. note:: This version is not yet released and is under active development.

.. _v0.7:

0.7 - November 14, 2017
~~~~~~~~~~~~~~~~~~~~~~~
* Add support for Python 3.6
* Add support for the InitialDate attribute
* Add server support for the GetAttributeList operation
* Add server support for the Locate operation
* Add client and server support for the MAC operation
* Add client and server support for the Revoke operation
* Add client and server support for the Encrypt operation
* Add client and server support for the Decrypt operation
* Add client and server support for the DeriveKey operation
* Add client and server support for the Sign operation
* Add client and server support for the SignatureVerify operation
* Add client and server support for retrieving wrapped keys
* Add client and server support for storing wrapped keys
* Add KMIP 1.4 enumerations
* Add server config option enabling certificate extension checks
* Add server config option defining set of usable TLS ciphers
* Add server config option setting the server log level
* Update the server to enforce checking object state and usage masks
* Update server Locate support to allow object name filtering
* Remove support for Python 2.6
* Fix bug with multithreading support with the SQLite backend
* Fix bug with how open() is mocked in the server test suite
* Fix bug with mismapped polymorphic identity for certificate objects
* Fix bug with socket interrupt handling under Python 3.5
* Fix bug with detached instance errors in the server test suite

.. _v0.6:

0.6 - December 14, 2016
~~~~~~~~~~~~~~~~~~~~~~~~~
* Add support for Python 3.5
* Add support for the State and OperationPolicyName attributes
* Add server support for the Activate and GetAttributes operations
* Add server support for certificate-based client authentication
* Add server support for object access control via operation policies
* Add server support for loading of user-defined operation policies
* Add client support for the GetAttributes operation
* Update clients to support operation policy names with objects
* Update ProxyKmipClient to support names when creating new objects
* Remove coveralls integration
* Fix bug with early server termination on missing request credential
* Fix bug with closing the client while unconnected to a server
* Fix bug with default values overriding server config file settings
* Fix bug with early server termination on bad client certificates
* Fix bug with deprecated usage of the bandit config file
* Fix bug with ProxyKmipClient registering unset object attributes

.. _v0.5:

0.5 - April 14, 2016
~~~~~~~~~~~~~~~~~~~~~~
* Add KmipServer server implementation
* Add KmipSession to manage threaded client/server connections
* Add KmipEngine for processing core server application logic
* Add KmipEngine support for CRUD operations for managed objects
* Add SQLAlchemy/SQLite support for KmipEngine data storage
* Add CryptographyEngine component for cryptographic operations
* Add pending deprecation warning for Python 2.6 support
* Add pending deprecation warning for the KMIPServer implementation
* Add support for building Sphinx documentation
* Add support for SQLAlchemy tables to all Pie objects
* Add Python magic methods to Attribute and Name objects
* Add Attribute class unit tests
* Add bin script to run the KmipServer
* Add setup entry points to run the KmipServer
* Update DiscoverVersions demo with optional versions argument
* Update all demo scripts to setup their own logging infrastructure
* Update README with information on the KmipServer implementation
* Remove expired certificate files from the integration test suite
* Remove default package log configuration and configuration file
* Fix bug with Locate payload parsing optional values
* Fix bug with DateTime string tests and move to UTC representation

.. _v0.4.1:

0.4.1 - December 2, 2015
~~~~~~~~~~~~~~~~~~~~~~~~
* Add support for the GetAttributeList operation
* Add integration with Travis CI, Codecov/Coveralls, and Bandit
* Add client/server failover support using multiple IP addresses
* Add additional attribute unit tests
* Update implementations of KMIP primitives
* Reorganize server code to prepare for refactoring
* Remove use of exec when handling library version numbers
* Remove broken server script

.. _v0.4:

0.4 - August 14, 2015
~~~~~~~~~~~~~~~~~~~~~
* Add the official Pie API for a simpler KMIP interface
* Add the ProxyKmipClient implementation of the Pie API
* Add key, secret, and opaque objects to the Pie object hierarchy
* Add unit demos for all ProxyKmipClient operations
* Add complete unit and integration test suites for the Pie package
* Add KMIPProxy client support/demos for the Activate and Revoke operations
* Add KMIPProxy client connection timeout support
* Add KMIPProxy integration tests for asymmetric key and secret/opaque objects
* Add improved request error logging for the KMIPServer
* Update README with additional information about the clients and Pie API
* Remove AUTHORS in favor of Git commit history
* Fix bug with dangling file handle when setting __version__
* Fix bug with dangling socket connection upon client destruction

.. _v0.3.3:

0.3.3 - June 25, 2015
~~~~~~~~~~~~~~~~~~~~~
* Add the core ManagedObject class hierarchy for the new Pie API
* Add updated Boolean primitive implementation and test suite
* Add integration tests for symmetric key creation and registration
* Update demo and client logging to log at the INFO level by default
* Update README with improved testing instructions
* Fix bug causing enumerations to be encoded as signed integers
* Fix bug with mismatched EncodingOption tag
* Fix bug with relative path use for version number handling
* Fix bug with Integer primitive breaking on valid long integer values

.. _v0.3.2:

0.3.2 - June 11, 2015
~~~~~~~~~~~~~~~~~~~~~
* Add support for registering and retrieving Certificates
* Update unit demos to work with Certificates
* Reorganize test suite into unit and integration test suites
* Remove old demo scripts
* Fix bug with incorrect KeyMaterialStruct tag
* Fix bug causing infinite recursion with object inheritance

.. _v0.3.1:

0.3.1 - April 23, 2015
~~~~~~~~~~~~~~~~~~~~~~
* Add KMIP profile information to the client
* Add support for registering/retrieving SecretData and Opaque objects
* Update the SecretFactory to build Public/PrivateKeys with user data

.. _v0.3:

0.3 - March 14, 2015
~~~~~~~~~~~~~~~~~~~~
* Add client support for the DiscoverVersions and Query operations
* Add client support for the CreateKeyPair and ReKeyKeyPair operations
* Add support for registering and retrieving PublicKeys and PrivateKeys
* Add unit demos demonstrating how to use individual KMIP client operations
* Add custom configuration support to the KMIP client
* Add inline documentation for new KMIP objects, attributes and payloads
* Add additional unit test suites for new KMIP objects, attributes and payloads
* Add dependency for the six library to handle Python version support
* Update README with a condensed description and breakdown of the library
* Fix bug with unindexed format strings (impacts Python 2.6)
* Fix missing certificate file issue when installing library from PyPI

.. _v0.2:

0.2 - November 17, 2014
~~~~~~~~~~~~~~~~~~~~~~~~~
* Add configuration file support
* Add client support for the Locate operation
* Update README with additional information and reStructuredText format

.. _v0.1.1:

0.1.1 - September 12, 2014
~~~~~~~~~~~~~~~~~~~~~~~~~~
* Fix bug with auto-installing third party dependencies

.. _v0.1:

0.1.0 - August 28, 2014
~~~~~~~~~~~~~~~~~~~~~~~
* Add support for Python 3.3 and 3.4
* Add support for KMIP client/server SSL connections
* Remove all Thrift library dependencies

.. _v0.0.1:

0.0.1 - August 12, 2014
~~~~~~~~~~~~~~~~~~~~~~~
* Initial release
* Add support for Python 2.6 and 2.7
* Add KMIP client and server
* Add client/server support for Create, Get, Register, and Destroy operations
* Add unit test suite

.. _`master`: https://github.com/openkmip/pykmip/