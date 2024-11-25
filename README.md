### To create keypair.pem file (can be safely removed once public/private keys are generated)
openssl genrsa -out keypair.pem 2048

### To create public key (for decryption)
openssl rsa -in keypair.pem -pubout -out public.pem

### To create private key (for encryption)
openssl pkcs8 -topk8 -inform PEM -outform PEM -nocrypt -in keypair.pem -out private.pem
