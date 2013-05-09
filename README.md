## repoman

An archlinux repo poking tool.

At the moment, a half baked and hacked together alternative to repo-add.

### Usage

    repoman -Us foo.db.tar.gz .

Add all packages in the current directory to foo.db.tar.gz and sign the
database with gnupg.

    repoman -V foo.db.tar.gz

Verify the packages foo.db.tar.gz refers to can be accessed and the
md5sum and sha256sum match.

    repoman -Q foo.db.tar.gz pkg ...

Print information about `pkg` much like how `pacman -Qi pkg` works

### TODO

- speed up archive updating.
    - provide a method of shallow db-parsing?
    - instead of reading in all the data and writing it out all over
      again, build up a set of operations to apply.
