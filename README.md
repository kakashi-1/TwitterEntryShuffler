# TwitterEntryShuffler
Random shuffler for twitter posts by sorting them by sha256(sha256(userhandle || nonce)).

This program is written in C++11

ShuffleEntries.cpp takes a list of tweet urls as input and outputs a file containing the user handles shuffled using a nonce constructed from the xor of a secret and a block hash.

The secret and block hash currently hardcoded into ShuffleEntries.cpp are just an example.

The double sha256 of the actual secret is 8dd4d706845ed329e7f4d3363f263e8e72d8d7b13c77dd1f4471f37c066b94ed.
The actual secret will be revealed after Bitcoin block 502961 is mined and the block hash of that block will be used to generate the nonce.

There's no makefile but the build is pretty straightfoward assuming you have C++11 support and the OpenSSL library installed. There's a build script included in the repo, but you might need to adjust the command for your environment.

Best of luck to all entrants!
