# Generating an SSH key
To generate a new key, just use this command:

`ssh-keygen -t rsa -C "<email address>"`

It'll prompt you for where to save the new file and also for a passphrase.

The key will be used automatically when you next try to SSH to that server with that email address. You can also set up an SSH alias with that username - see other SSH notes.

Source: [drupal.org](https://www.drupal.org/node/1070130)

Further reading: [ietf.org](http://www.ietf.org/rfc/rfc4716.txt)

#macos #ssh