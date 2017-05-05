
# GnuPG Usage

## Using practice keys in class

### Download https://people.rit.edu/djaigm/hfoss/pubring-S17.gpg to local machine

  * ```gpg --import pubring-S17.gpg```

### Import your secret practice key 

  _**DEADBEEF.sec** here is an example filename, use your own in its place_

  * ```gpg --import DEADBEEF.sec```

### Sign a public key from the keyring 

  _**00FADED** here is an example key ID. Use one from the list you imported in its place._

  * ```gpg --sign-key 00FADED```

### Export the public key you signed

  * ```gpg --export -a 00FADED > 00FADED-signed.asc```

### Send the exported key file to the instructor and to the holder of the private key

## Participate in the class keysigning

### Generate your own key

### Send the key fingerprint to the instructor

### Make available the public key 

You can do one of two things

  * export key as an ASCII armored file and send to other keysigning participants (in this case, the instructor suffices)
  * upload your key (via ```gpg --send-key DEADBEEF ```) to a keyserver


### Charles Profitt's series on using GnuPG from Fedora Magazine

    https://fedoramagazine.org/gnupg-a-fedora-primer/

    https://fedoramagazine.org/gpg-using-your-key/

    https://fedoramagazine.org/gpg-key-management-part-1/

    https://fedoramagazine.org/gpg-key-management-part-2/

### Video demonstrating creating a new keypair at the commmand line:

http://people.rit.edu/djaigm/www/gpg-demo/gen-key-demo.webm


### Captures of a GnuPG command-line session in GNU/Linux

http://people.rit.edu/djaigm/gpg-demo/scripts/rot13-caesar-demo.html

http://people.rit.edu/djaigm/gpg-demo/scripts/symmetric-demo.html

http://people.rit.edu/djaigm/gpg-demo/scripts/gen-key-demo.html

http://people.rit.edu/djaigm/gpg-demo/scripts/display-keys.html

http://people.rit.edu/djaigm/gpg-demo/scripts/export-demo.html

http://people.rit.edu/djaigm/gpg-demo/scripts/sign-key.html

http://people.rit.edu/djaigm/gpg-demo/scripts/sign-verify-demo.html

