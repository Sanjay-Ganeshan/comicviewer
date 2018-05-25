A simple placeholder-webpage to display web comics in.

# Setting up

First, download this repo using `git clone`. Place the contents of this repo somewhere into your site.

Find the "CHANGE THIS" comment in comicViewer.html. Replace the comicFolder variable with 
the relative path (from base url) to the "comics" folder. In this example, since the comics
folder is "/comics/", we have set this variable to "/comics/"

# Adding a new comic

Give your comic a name (id), without spaces or special characters (all lowercase letters is nice).
Create a new folder with this id in the `comics/` directory. (See: `comics/madoka`, `comics/notmadoka`, `comics/example`).

Add each page to the folder, with the names `page1.jpg`, `page2.jpg` ... `page25.jpg` so on and so forth.
They should all take the form `page_.jpg` (fill in the blank).

Now, go to `comics/info.txt`, and ensure it is correct. For each folder in the `comics/` directory (each comic id),
there should be a single line in `info.txt` with the comic id followed by the number of pages in the comic, seperated 
with a `|` character. (For example: `example|3` means there is a comic called "example" with 3 pages).

Note that the page numbers should always begin at 1.

Now `comicViewer.html` will give you a comic viewer!

## Notes

The "Link to this page" link will only work in Chrome, Firefox, Safari, and Opera, since it 
uses the `URLSearchParameters` javascript class (not implemented in Edge).

The links take the form `comicViewer.html?comic=name&page=number`.

