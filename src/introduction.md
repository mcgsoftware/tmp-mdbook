# Introduction

This is a book on Go notes. 

<img src="./images/golang-gopher.svg" alt="Alt Text" width="500" height="200">

# Making the mdbook a ghpages

## 1. stop the mdbook server if its running. 

## 2. Comfigure mdBook target directory

To configure mdBook to use /docs as the target directory instead of the default /book, follow these steps:

### Step A: Modify the book.toml Configuration File

The book.toml file is used to configure your mdBook project. You need to update it to set /docs as the build directory.

-	Open the book.toml file in the root of your mdBook project.

-	Add or modify the [build] section to specify the output directory:

```
[build]
build-dir = "docs"
```

### Step B: Rebuild the Book

Run the mdbook build command to regenerate the book, now targeting the /docs directory:
```
mdbook build
```

This will create the static files in the docs/ directory.

### Step C: Verify the Change

Check the docs/ directory to ensure the built book is there.

### Step D: Push to GitHub (if hosting via GitHub Pages)


1.	Commit and push the changes to your repository:

```
git add .
git commit -m "Update mdBook to use docs as target directory"
git push
```


2.	If you’re hosting on GitHub Pages:
	•	Make sure GitHub Pages is set to serve the /docs folder as described in the previous steps.

## Notes:

•	Changing the build-dir to /docs is helpful when using GitHub Pages, as it avoids manually moving the contents of the /book directory.

•	Every time you build the book, mdBook will now output the files directly to /docs.

## Enable GitHub Pages

	1.	Go to your repository on GitHub.
	2.	Navigate to Settings > Pages.
	3.	Under Source, select the main branch and set the folder to /docs.
	4.	Save the settings.

## Access Your Book

After enabling GitHub Pages, your book will be available as a website at:
```
https://username.github.io/repo-name

https://mcgsoftware.github.io/tmp-mdbook/
```