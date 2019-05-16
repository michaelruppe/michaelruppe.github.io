## This is the code for my website

## Organising project sources
Where possible, pages in a \_Collection will simply load a <script> from its prespective github repo, eg:

`<script src="michaelruppe.github.io/repo/script.js">`

This works fine for scripts that have no external assets (images, json files etc).
In the case where there is an external asset, the entire contents of the script directory are directly copied into the page directory. This preserves the relative file paths used within the script eg `imgBird = loadImage('assets/bird.png');` which keeps the script repo transportable. That is, you don't have to use lines like `imgBird = loadImage('user.github.io/repo/assets/bird.png');` which is pretty awful if somebody wants to copy it and execute locally.
