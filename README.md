# Dummy-release-test
Release GHA are plaguing me, so this repo is for testing purposes

There seems to be various ways that releases are built, so we will find
out how this goes.

Some primary triggers of the workflows seems to be with tags, so let's
start with an an initial release using a git tag.

# General Notes:

## v0.0.1 - v0.0.2

Oops forgot to push the tags

## v0.0.3

The artifacts didn't go through, but that may be a problem with forgetting to add them.

Furthermore, Windows was broken due to not adding .exe to the end of the file, so trying
to add a wildcard on there.

## v0.0.5

This one errored out because I accidentally left commas after "stable" in the Rust version
and I foolishly tried to commit --amend it, but that's not a good idea with tags.

## v0.0.6

There's an issue with the files being downloaded from the download action and how they are
being handled by the release-action.

Both appear to recommend to tar the files, so let's see if that works.

## v0.0.8

Not currently convinced that the previous methods have been the best
idea. Even if they were to work. Currently the files are not a tarball.
Found some actions from `taiki-e` and thought that they may be worth the
try.

## v0.0.10

HOLY HELL, taiki-e is a genius. Not entirely sure what black magic is
there. I'll have to take a look at the scripts, but we are published
with compression.

Now it's just time to get the changelog working.

I realized that I wasn't sending my local commits up to remote, so let's
first test that.

## v0.0.11

I forgot to change the CHANGELOG.md -> BODY.md

I really think I should probably be echoing body too just to ensure that
it's there, but let's see.

## v0.0.14

At this point, everything more or less works. Although, the best answer
for properly building out the change log has yet to be determined, but
there is a path forward, so that's nice.

Now it's time to make sure the `-rc` workflow will work without
triggering a regular release.
