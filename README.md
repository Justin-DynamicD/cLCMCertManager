# cLCMCertManager
DSC Module and Resource to compare configured thumbprint to desired certificate

This module and resource will select a local machine certificate based on the provided filter cirteria then compare the thumbprint to the thumbpring configured in the LocalConfigurationManager.  If the the two do not match, it exports the appropriate certificate to the defined location using the machine name (short or FQDN) to a specified location so it may be used by configurations in future mofs.

Note this is not a complete solution to expiring/reewing certificates.  During the configuration process, the build script should check the same location for certificates to be used when encrypting passwords/mofs.  Including a meta-mof will allow the pull server to specify updated thumbprints as they change.
