# gim

A simple bash script for transparent editing of gpg-encrypted files.

## Installation

Clone the repository

  git clone https://github.com/jwergieluk/gim.git

Edit the `gim` file to adjust the configuration. Specifically, replace
the GPG_RECIPIENT value with the hash of your public key, which can be
obtained by issuing the command

    gpg --list-keys

Example output:

    pub   rsa4096/0xFD39274CDBCF703C 2013-06-17 [SC] [expires: 2021-07-07]
    Key fingerprint = FEB4 4E0D 0AA2 BCFD B9B6  0881 FD39 274C DBCF 703C

Mark the `gim` script as executable and copy to a location included in
your `PATH` variable:

    chmod +x gim
    cp gim "$YOUR_SCRIPTS_DIR"

## Usage

From command line prompt:

    gim secrets.txt.gpg

The script will create a temporary plain text file, open the file with 
the editor specified in the configuration, and encrypt the plain text file
after the editor finishes.

## Copyright and license 

`gim` is released under the GNU GENERAL PUBLIC LICENSE Version 2. See LICENSE file for details.

Copyright (c) 2015--2019 Julian Wergieluk


