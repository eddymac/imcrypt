# IM Crypt Utilities

A suite of encryption routines in a self contained HTML file that can be used
with Instant Messaging programs, such as Twitter, Facebook Messanger, and even
Reddit and the such.

The prime motivation for writing this is to demonstrate how futile attempting
to pohibit use of ncryption technologis through legislation is. It also though
has more practical uses, including assisting in educating people regarding
encryption. It can also be used for privacy and authentication where no other
method is available.

The program itself is written using raw HTML, CSS and Javascript. Currently it
makes use of Javascript's "Bigint" facility, which is specified in ECMA262. The
HTML file is completely self contained. There are no links to any other files.
It can be, and should be, downloaded to local disk or storage and run from
there. It can even be run without a network connection.

This should be able to run on modern versions (or later) of:

* On the Desktop:
  * Google Chrome version 67
  * Microsoft EDGE version 79
  * Firefox version 68
  * Opera version 54
  * Safari version 14
* On mobile devices:
  * WebView Android version 67
  * Google Chrome Android version 67
  * Firefox Android version 68
  * Opera Android version 48
  * iOS Safari version 14
  * Samsung Internet version 9.0
* On the server (modifications needed as it is designed with user interface):
  *  Node.js version 10.4.0

Should requirement arise, I will put a pure javascript replacement routine in
for the "Bigint" functionality, which would cater to much older browsers. Even
without that this routine should be able to run on about 99% of the computers
out there, incluing mobile devices.

The encryption technologies employed are:

SHA 256 for the hash algorythm
AES 256 for ciphering and deciphering
Eliptic Curve secp256k1 for the private/public key mechanism, then ECDH and ECDSA
Various block ciphers user can choose for encryption, including OFB, CFB. CTR,
CBC and PCBC, as well as a special one "CTRB" which is like CTR except it XORs
before ciphering rather than after.
