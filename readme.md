## CSR

The server configuration file contains a Certificate Signing Request (CSR) section that can be configured. The following is a sample CSR.

cn: fabric-ca-server
names:
   - C: US
     ST: "North Carolina"
     L:
     O: Hyperledger
     OU: Fabric
hosts:
  - host1.example.com
  - localhost
ca:
   expiry: 131400h
   pathlength: 1

A certificate signing request (CSR) is one of the first steps towards getting your own SSL/TLS certificate. Generated on the same server you plan to install the certificate on, the CSR contains information (e.g. common name, organization, country) the Certificate Authority (CA) will use to create your certificate. It also contains the public key that will be included in your certificate and is signed with the corresponding private key. We’ll go into more details on the roles of these keys below.

https://www.globalsign.com/en/blog/what-is-a-certificate-signing-request-csr
