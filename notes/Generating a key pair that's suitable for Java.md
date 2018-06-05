# Generating a key pair that's suitable for Java
First, generate the RSA-2048 key pair in PEM format.

`$ openssl genrsa -out keypair.pem 2048`

Convert the public key to RSA DER format:

`$ openssl rsa -in keypair.pem -outform DER -pubout -out public.der`

Convert the private key to PKCS8 DER format:

`$ openssl pkcs8 -topk8 -nocrypt -in keypair.pem -outform DER -out private.der`

Source: [stackoverflow.com](https://stackoverflow.com/questions/24338108/java-encrypt-string-with-existing-public-key-file)

#crypto #java