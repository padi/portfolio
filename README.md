# portfolio site

Simply put, it takes index.html and serves it to ignifymedia.github.io.

One can easily edit the index.html and other assets by hand,
but I use Mobirise version 5.6.5 to rapidly iterate
the content and feel of the site

Just "Publish" to "Local Drive Folder" and check in the resulting changes in git,
and push to `main` branch to update changes live.

## How to update the website when Github integration doesn't work

```
TL;DR: upload manually to Github repository and setup
`main` branch as the default Github Pages branch.
```

Here is a workaround until Mobirise fixes the bugs. The following details how to upload manually to Github.
Once you are familiar with the steps it takes roughly 2 minutes to do.

1. Create the repository on your github that you will use to host the site. (if it doesn't already exist)
2. Tell mobirise to `Publish` to a `Local Drive Folder`, instead of Github. Make sure this is a new empty folder where you will remember its location.
3. Open the intended Github repository in your browser
4. Open the folder on your computer where the site was published
5. Back at the Github repository, select Add File > Upload Files

You should now see a box where you can drop the files you want to upload

6. Back at the Folder where you have the new site, select all of the items and drop them into that box shown above. (Note: You do not have to delete any existing files from the repository, you uploading same-named files will overwrite old ones.)
7. Select "Commit Changes" and let Github process the upload.
8. Once that is done, go to the repository's Settings
and scroll down to the "GitHub Pages" section. Make sure that the branch is either Master or Main (depending on how you have it set). You can find out which branch to select by looking at where the files uploaded and check the name of the branch they are located (circled in blue)

9. Your site should now be live. You can check its deployment at https://[yourusername].github.io/[yoursiterepository]/, or you can go to your connected Domain and you should see it uploaded.

Source: Source: https://forums.mobirise.com/discussion/comment/78541/#Comment_78541

## Remove hidden links generated by Mobirise

Just run `./remove_mobirise_links.rb` script [needs ruby installed].
If new links are generated in `./asset/theme/js/script.js`,
you can include more strings in blacklist.txt
