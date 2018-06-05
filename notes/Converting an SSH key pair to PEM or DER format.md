# Converting an SSH key pair to PEM or DER format
See also [[Generating an SSH key]].

The normal ssh-keygen process creates a pair of keys which are fine for ssh, but may not be suitable for all purposes.

To convert a key to PEM format:

`ssh-keygen -f ~/.ssh/id_rsa.pub -e -m PEM > ./id_rsa.pub.pem`

To convert a key to PCKS-8 format:

`ssh-keygen -f ./env1_rsa.pub -e -m pkcs8 > id_rsa.pub.pk`

To convert a PEM to a DER:

`openssl rsa -RSAPublicKey_in -in ./id_rsa.pub.pem -inform PEM -outform DER -out ./id_rsa.pub.der -RSAPublicKey_out`

Source: [unix.stackexchange.com](https://unix.stackexchange.com/questions/220354/how-to-convert-ssh-public-key-from-pem-to-der-format)

#crypto #ssh