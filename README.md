# textexpander-dates-nextday

[![Semantic Versioning](https://img.shields.io/github/release/davidwaterston/textexpander-dates-nextday.svg)](http://semver.org/)
[![MIT Licence](http://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/davidwaterston/textexpander-dates-nextday/blob/master/LICENSE)
[![Releases signed with Gnu Privacy Guard](https://img.shields.io/badge/gpg-signed-green.svg)](#verifying-releases)

A small group of [TextExpander](https://smilesoftware.com/TextExpander/index.html) snippets that can be used to quickly and easily insert any date in the next week into a document, by referencing it by name. For example, to insert the date of the next Friday after the current date, simply type _;nfri_.

![textexpander-dates-nextday in action](https://raw.githubusercontent.com/wiki/davidwaterston/textexpander-dates-nextday/images/dates1.gif)

The following shortcuts are included:

| Date | Shortcut |
|---|---|---|
| Next Monday | ;nmon |
| Next Tuesday | ;ntues |
| Next Wednesday | ;nwed |
| Next Thursday | ;nthurs |
| Next Friday | ;nfri |
| Next Saturday | ;nsat |
| Next Sunday | ;nsun |



## Installation

To install these snippets:

- Open TextExpander
- Click the + sign in the bottom left of the dialog and select _Add Group from URL..._ (or press ⌘ - L)
- Paste in the following URL: https://raw.githubusercontent.com/davidwaterston/textexpander-dates-nextday/master/dates-nextday.textexpander
- Press _OK_

After a few seconds a new group named _Dates: Next Day_ will appear; your new snippets are ready to use!

## Changing the formatting of the dates
By default dates are displayed using the format _full day, full month, dd_, for example _Monday, July 13_. If you prefer a different date format you can change this simply by editing the snippet.
Each snippet will look like this:
```
%snippet:util.+getNextDayOfWeek+%%A, %B %e
```
The first part - _%snippet:util.+getNextDayOfWeek+%_ - should never be changed. The second part - _%A, %B %e_ - is the date formatting and can be modified to suit your requirements. For example:
```
%snippet:util.+getNextDayOfWeek+%%m/%d/%y
```
will return the date in _mm/dd/yy_ format, for example _07/17/15_.
More information about the extensive date formatting options can be found [on the TextExpander website](https://smilesoftware.com/help/TextExpander/datetime.html).


## What's this weirdly named snippet? It doesn't seem to do anything.
In the _Dates: Next Day_ group is an oddly named snippet called _util.+getNextDayOfWeek+_. This is a small snippet of Javascript used to calculate the date of the next _whatever day you want_. It's used by all of the other snippets in the group and shouldn't be deleted.
The unusual name is simply so that it's unlikely you would type it by mistake, causing TextExpander to try and replace the text.

## Compatibility
These snippets have been tested and confirmed to work with TextExpander version 5.01 and later. As they make use of the new ability to write snippets in Javascript, it's unlikely they will work in earlier versions.


## Release History
See the [change log](https://github.com/davidwaterston/textexpander-dates-nextday/blob/master/CHANGELOG.md) file for more details.


## Verifying Releases
I use <a href="http://semver.org" target="_blank" alt="Semantic Versioning">Semantic Versioning</a> to number releases. Each release is tagged with the appropriate version number and signed using <a href="https://www.gnupg.org" target="_blank" alt="Gnu Privacy Guard (GPG)">Gnu Privacy Guard (GPG)</a>. The public key used to sign releases is
```
Name: David Waterston
Email: david@davidwaterston.com
Key ID: A7AD9C85
Signature: 71A9 DC13 447A 1E4F C6EB  5D64 DE08 A991 A7AD 9C85
```
This public key is included in the repository with a SHA1 of 16d013451476fa4a1a67d6ad4b90583e205b53b1.
After cloning the repo, and assuming you have GPG installed correctly, you can import this key into your keychain
```
git cat-file blob pubkey | gpg --import
```
When this public key is successfully imported, you can use it to verify the integrity of any of the tagged releases of this repo
```
git tag -v v1.0.0
```
which should produce output similar to:
```
object 04f37a55784c1f3abc2cf927a935a488aa954035
type commit
tag v1.0.0
tagger David Waterston <david@davidwaterston.com> 1427387056 +0000

Initial commit

This is just an example so don't get fixated on the details, what matters is the signature!
gpg: Signature made Thu 26 Mar 16:24:16 2015 GMT using RSA key ID A7AD9C85
gpg: Good signature from "David Waterston <david@davidwaterston.com>" [ultimate]
```
The important thing to notice here is that the RSA key ID matches mine (A7AD9C85) and the line that says that this is a good signature.

The public key can further be verified by checking the details held on <a href="http://pgp.mit.edu/pks/lookup?search=david%40davidwaterston.com&op=index&fingerprint=on&exact=on" target="_blank" alt="pgp.mit.edu">pgp.mit.edu</a>.


## License
Copyright (c) 2015 David Waterston. All rights reserved.
Distributed under an MIT license. See the [LICENSE](https://github.com/davidwaterston/textexpander-dates-nextday/blob/master/LICENSE) file for more details.
