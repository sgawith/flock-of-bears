# Unpacking a .deb file on macOS
You'll need to install dpkg first:

`brew install dpkg`

After that, you can list the contents of the package:

`dpkg -c <path/package>`

Or you can extract the contents of the package:

`dpkg -x <path/package> <output_path>`

Source: [ericwilson.io](https://ericwilson.io/snippets/2015/10/11/how-to-unpack-a-deb-file-on-mac-os-x-without-installing-it)

#macos #linux #dpkg