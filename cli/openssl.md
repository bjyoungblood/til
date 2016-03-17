##### Working with keys, certificates, and CSRs

```
# CSR with new private key
openssl req -out /path/to/csr -new -newkey rsa:2048 -nodes -keyout /path/to/privatekey`

# Self-signed cert with new private key
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout /path/to/privatekey -out /path/to/certificate

# CSR from existing key
openssl req -out /path/to/new.csr -key /path/to/private.key -new

# CSR from existing key and certificate
openssl x509 -x509toreq -in /path/to/certificate -out /path/to/new.csr -signkey /path/to/private.key

# Print certificate info
openssl x509 -in /path/to/certificate.crt -text -noout
```
