# wacs-sert-create-for-IIS


router: 192.168.88.251:80 -> 192.168.88.250:80


https://trueconf.ru/blog/baza-znaniy/sozdanie-sertifikata-lets-encrypt-na-windows.html


---------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------

Please choose from the menu: M

 Running in mode: Interactive, Advanced

  Please specify how the list of domain names that will be included in the
  certificate should be determined. If you choose for one of the "all bindings"
  options, the list will automatically be updated for future renewals to
  reflect the bindings at that time.

 1: IIS
 2: Manual input
 3: CSR created by another program
 C: Abort

 How shall we determine the domain(s) to include in the certificate?: 2

 Enter comma-separated list of host names, starting with the common name: directumdm.ru

 Target generated using plugin Manual: directumdm.ru

 Suggested friendly name '[Manual] directumdm.ru', press <ENTER> to accept or type an alternative: <Enter>

  The ACME server will need to verify that you are the owner of the domain
  names that you are requesting the certificate for. This happens both during
  initial setup *and* for every future renewal. There are two main methods of
  doing so: answering specific http requests (http-01) or create specific dns
  records (dns-01). For wildcard domains the latter is the only option. Various
  additional plugins are available from https://github.com/win-acme/win-acme/.

 1: [http-01] Save verification files on (network) path
 2: [http-01] Serve verification files from memory
 3: [http-01] Upload verification files via FTP(S)
 4: [http-01] Upload verification files via SSH-FTP
 5: [http-01] Upload verification files via WebDav
 6: [dns-01] Create verification records manually (auto-renew not possible)
 7: [dns-01] Create verification records with acme-dns (https://github.com/joohoi/acme-dns)
 8: [dns-01] Create verification records with your own script
 9: [tls-alpn-01] Answer TLS verification request from win-acme
 C: Abort

 How would you like prove ownership for the domain(s) in the certificate?: 2

  After ownership of the domain(s) has been proven, we will create a
  Certificate Signing Request (CSR) to obtain the actual certificate. The CSR
  determines properties of the certificate like which (type of) key to use. If
  you are not sure what to pick here, RSA is the safe default.

 1: Elliptic Curve key
 2: RSA key

 What kind of private key should be used for the certificate?: 2

  When we have the certificate, you can store in one or more ways to make it
  accessible to your applications. The Windows Certificate Store is the default
  location for IIS (unless you are managing a cluster of them).

 1: IIS Central Certificate Store (.pfx per domain)
 2: PEM encoded files (Apache, nginx, etc.)
 3: Windows Certificate Store
 4: No (additional) store steps
 C: Abort

 How would you like to store the certificate?: 1

 Path to Central Certificate Store: C:\wacs\crt\090622

 Password to use for the PFX files, or enter for none:

 1: PEM encoded files (Apache, nginx, etc.)
 2: Windows Certificate Store
 3: No (additional) store steps
 C: Abort

 Would you like to store it in another way too?: 3

  With the certificate saved to the store(s) of your choice, you may choose one
  or more steps to update your applications, e.g. to configure the new
  thumbprint, or to update bindings.

 1: Create or update https bindings in IIS
 2: Create or update ftps bindings in IIS
 3: Start external script or program
 4: No (additional) installation steps

 Which installation step should run first?: 4

 Existing renewal:    [Manual] directumdm.ru - renewed 1 time, due after
                      2022.7.2 15:07:03

 Overwrite? (y*/n)  - yes

 Overwriting previously created renewal
 Authorize identifier: directumdm.ru
 Authorizing directumdm.ru using http-01 validation (SelfHosting)
 Authorization result: valid
 Requesting certificate [Manual] directumdm.ru
 Store with CentralSsl...
 Copying certificate to the Central SSL store
 Saving certificate to Central SSL location C:\wacs\crt\090622\directumdm.ru.pfx
 Installing with None...
 Removing certificate from the Central SSL store
 Scheduled task looks healthy
 Next renewal scheduled at 2022.8.3 10:26:07

 N: Create new certificate (simple for IIS)
 M: Create new certificate (full options)
 R: Run scheduled renewals (0 currently due)
 A: Manage renewals (4 total)
 O: More options...
 Q: Quit

 Please choose from the menu:
