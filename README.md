Certificate Authority Administration
====================================

CA-Admin is a wrapper around some openssl-scripts, to simplify the
administration of setting up and maintaining a certificate authority.

Use the CA-admin script for all certificate administration.

Usage 
-----
    CA-admin <command>

Commands:

 `init`   - Initialize the Certificate Authority by creating key, cert, directory 
            structure, index and serial files.
            

 `new`    - Create new certificate. This command has two sub-commands: server (for
            generating a server certificate) and client (client certificate).

 `list`   - List certificates issued by this CA. Use sub-command to display 
            servers, clients or all certificates.

 `show`   - Display details for given certificate.

 `revoke` - Revoke a certificate and update the CRL.

 `crl`    - Certificate Revocation List (CRL) specific sub-commands: show (display
            ascii contents of current CRL), generate (create an updated CRL), 
            publish (copy CRL to CRL_PUB_{DER|PEM} as specified in etc/config).

Notes
-----

Configuration file located in `./etc/config`.

Do not modify any of the files in the `CABASE` directory manually, files like the index are very fragile.

