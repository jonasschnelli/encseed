[![Build Status](https://travis-ci.org/jonasschnelli/cipherseed.svg?branch=master)](https://travis-ci.org/jonasschnelli/cipherseed) 

cipherseed
=====

128bit entropy
----------------
1 byte header unencrypted
5 byte unencrypted pbkdf2-salt
3 byte header encrypted (1 bit version, 15 bit birthday, 8 bit type)
16 byte encrypted entropy
<<<<<<< Local Changes
4 byte primary MAC tag (tag covers salt || encrypted header || encrypted entropy)
4 byte secondary MAC tag (tag covers salt || encrypted header || encrypted entropy)
= Total 33 bytes
=======
4 byte primary MAC tag
4 byte secondary MAC tag
= Total 33 bytes (== 264 bits ~== 24 word mnemonic ~== 53 base32 chars without checksum)
>>>>>>> External Changes

256bit entropy
----------------
1 byte header unencrypted
5 byte unencrypted pbkdf2-salt
3 byte header encrypted (1 bit version, 15 bit birthday, 8 bit type)
32 byte encrypted  entropy
<<<<<<< Local Changes
4 byte primary MAC tag (tag covers salt || encrypted header || encrypted entropy)
4 byte secondary MAC tag (tag covers salt || encrypted header || encrypted entropy)
= Total 49 bytes
=======
4 byte primary MAC tag
4 byte secondary MAC tag
= Total 49 bytes (== 392 bits == 36 word mnemonic == 79 base32 chars without checksum)
>>>>>>> External Changes


Fields
1 byte header unencrypted: allows to upgrade encryption scheme
5 byte unencrypted pbkdf2-salt
