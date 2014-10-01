# go-passwords

*Encrypt user passwords in Go.*


## Meta

- Author: Randall Degges
- Email: r@rdegges.com
- Twitter: [@rdegges][]
- Site: http://www.rdegges.com
- Status: in development


## Purpose

Properly hashing user passwords is important for any application that stores
user data.  By properly hashing user passwords, you're providing your users with
a more secure and safe experience.

Unfortunately, there are many ways to hash user passwords, and information on
the subject is not widely known and discussed in the programming world.

By using this password hashing library you'll be able to:

- Easily hash user passwords in the safest possible way.
- Easily upgrade your user password hashes as cryptographic technology improves
  over time.

This library takes a highly opinionated approach to user password security --
providing you with only the most basic possible API for hashing, and verifying
user passwords.

As time passes and CPUs become stronger, this library will allow you to
transparently upgrade your user's password hashes to stronger algorithms.


## Technologies

This library uses the [scrypt (pdf)][] hashing algorithm to securely and safely
hash user passwords.

scrypt is widely considered the strongest possible hashing algorithm as it
requires a significant amount of both CPU *and* memory resources to compute a
hash.  This makes it substantially harder for attackers to reverse (*brute
force*) any scrypt password hashes, as it requires a significant amount of
computational resources.

The scrypt crypto implementation used by this library is written by the Go core
developers -- and is part of the [go.crypto][] project.  It is implemented in
pure Go based on the [scrypt (pdf)][] specification published by
[Colin Percival][].


  [@rdegges]: https://twitter.com/rdegges "Randall Degges on Twitter"
  [scrypt (pdf)]: http://www.tarsnap.com/scrypt/scrypt.pdf "scrypt pdf"
  [go.crypto]: https://code.google.com/p/go/source/browse?repo=crypto "go.crypto"
  [Colin Percival]: http://www.daemonology.net/ "Colin Percival's Personal Website"
