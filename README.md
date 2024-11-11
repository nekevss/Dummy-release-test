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

Not currently convinced that the previous methods have been the best idea. Even if they were
to work. Currently the files are not a tarball. Found some actions from `taiki-e` and thought
that they may be worth the try.