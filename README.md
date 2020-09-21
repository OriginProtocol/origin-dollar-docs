## Purpose

This repo is for syncing the documentation for Origin Dollar between Gitbook and Crowdin, which we use for translations.

## Editing

All edits and improvements to the documentation should be made at https://docs.ousd.com. If you're a core team member, you can find an invite link to Gitbook in a pinned message in the internal Origin Dollar Discord channel.

Gitbook tracks each translation in "variants" which map to different branches on Github. Crowdin pushes the various translations to named folders on the translations branch. For now, it's a manual process to move the latest translations from the folders to their matching branches.

## Translation flow

Here's the process by which our OUSD docs are translated:

- Edits to the docs should be made on the English version of the docs on Gitbook. This is considered our canonical source.
- Gitbook will sync the `en` branch to Github when you save & merge
- Crowdin will fetch the `en` branch every ten minutes to check for changes
- Our translators will submit their translations on Crowdin
- Crowdin will push the new translations in the form of a pull request on the `translations` branch
  - Crowdin will put each translation in a different folder named with the language code
  - However, Gitbook expects the different translations to be in seperate branches with the files at the root. Until we write a script for this, you'll need to manually go through each language branch, and copy the files from the `translations` branch into the right place.

# Updating the translations

Use the following steps to push the latest translations to Gitbook. For example, to update the Chinese docs:

 - Clone the repo and fetch all remote branches
 - Merge the latest changes from the `translations` branch into the `zh` branch
 - Move everything in the `/zh` folder into the root directory and delete everything else. Once you're done, you should see a Chinese version of README.md in the root directory.
 - Add and commit everything and push the `zh` branch to Github
 - Go to Gitbook and confirm everything updated as expected. It may take a minute or two for the changes to sync.  

# Adding a language

To add a language in Gitbook:

- Create a new variant
- Set the slug to the two letter country code for the language
- Make sure to set the local user interface in Gitbook if it is available
- Add the language in Crowdin & recruit translators
- Add a new branch in Github that uses the same two letter language code that was set in Gitbook

## Volunteer

Volunteers who wish to help improve our translations can volunteer using this form:
https://goo.gl/PqT326


