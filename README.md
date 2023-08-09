# Bitbucket backup

[![Build Status](https://travis-ci.org/samkuehn/bitbucket-backup.svg?branch=master)](https://travis-ci.org/samkuehn/bitbucket-backup)

## Description

This python script will backup all of your Bitbucket repos locally.
If the repository does not exist locally the repo will be cloned to the <local_backup_location>.
If the repo does exist locally an `git remote update` will be run for git repos.

It's just a quick fork of [https://github.com/samkuehn/bitbucket-backup]() to make it work with modern BitBucket api.

## Installation

```bash
pip install -U https://github.com/samkuehn/bitbucket-backup/archive/master.zip
```

## Quickstart

```bash
bitbucket-backup [-u <bitbucket_username>] [-p <bitbucket_password>] [-x <auth_token>]
  [-l <local_backup_location>] [-t <bitbucket_team>] [-a] [-v] [-q] [-c] [--http] [--skip-password] [--mirror]
  [--prune] [--fetchlfs]
```



Firstly you will need to create an access token - see this answer - [https://stackoverflow.com/a/73072175]()

Then you will need to pass this token as `-x` argument
Clone/update requires that your SSH keys have been uploaded to Bitbucket.

You can backup a team's repositories instead of your own by supplying the optional `-t` parameter
and entering the team slug (this is now called a "Workspace" by BitBucket).

## Requirements

You do need to have your SSH keys uploaded for the computer that you are running the backup on.

## Additional notes

I am hosting this on GitHub because I believe it is superior for public repos (I understand the irony).
