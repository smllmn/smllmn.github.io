---
layout: post
title: On keybase and trust
categories: ["keybase", "trust", "digital security"]
---
You may have noticed the shiny little [keybase.io](keybase.io) icon at the 
bottom of my website. You may even have clicked on it. If you haven't, take a
quick look.

On that profile, there are a number of _verified_ accounts and the like,
including my [twitter](twitter.com/smllmn), [github](github.com/smllmn) and
this website. Verified, in this case, means that there exists a publicly
available demonstration that I both control that account and the private key
whose corresponding public key is available on the keybase profile.

If that
last sentence didn't make much sense to you, don't worry, it's fairly
straightforward: public-key encryption is a system of two keys. Individuals
(and organisations) have pairs of keys, one of which is private and known only
to them, and the other of which is public and known to the world. The beauty is
that the two keys can undo encryption by the other. That is, anything I encrypt
with my private key can be decrypted with my public key, and anything that is
encrypted with my public key can be decrypted with my private key. This clever
little system is what makes most of the modern internet work, from online
banking to secure communication with your friends.

The idea behind keybase is to provide a centralised system for proving identity
using public-key cryptography. With a public and private key pair, it's
straightforward to prove ownership of an online account. On twitter, for
instance, you simply post something encrypted with your private key and anyone
with your public key can decrypt it and verify it's really you. The problem has
always been that phrase "anyone with your public key". Perhaps I need cooler
friends, but no-one has ever actually given me their public key (and if I'm
being open, I've never given anyone mine either). Here's where keybase comes
in: it provides a centralised place to host a public key that the whole world
can see.

It's not without its problems, though. The _smllmn_ keybase account has proven
that they own this domain and the other accounts listed on that page, but do
you know for certain that the owner of this domain and those accounts is
actually Luke Smallman? Unless you've met him in person and he has verified
that he owns one of those accounts, you can't be sure. If you have and you are
sure, though, the miracle of public key cryptography means you can also be sure
that this is me writing here. Hi!

Overall, I like keybase. It's got loads of features I've not covered here, 
including encrypted file-sharing via the keybase file system, and it solves an
annoying problem which made publicly verifying your identity difficult. I'd
love to see it pick up some more steam. If you're interested, it's currently
in closed-beta but I've got some invites available. If you want one, send me a
message on one of my verified social media accounts ;)
