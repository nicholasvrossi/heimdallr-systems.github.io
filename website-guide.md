---
layout: default
title: Editing the website
author: roper
---

# Editing the website

*Note: Before going through this guide, read the guide on [Getting Started with Git and GitHub](git-guide.html)*

All of the files that make this website work on stored in a
[single repository on GitHub](https://github.com/heimdallr-systems/heimdallr-systems.github.io/).
All of the pages in the website are written in [Markdown](https://en.wikipedia.org/wiki/Markdown). When a new commit is
made to the repository, [GitHub Pages](pages.github.com) uses the [Jekyll](https://jekyllrb.com/) static site generator
to generate a complete set of HTML and CSS files, which are then published to
[heimdall-robot.github.io](heimdall-robot.github.io)

## Adding pages

To add a page to the website, create a new [Markdown](https://en.wikipedia.org/wiki/Markdown) file in this
repository (do not worry about forking it like do for most repositories, you can edit directly in this one).
The only difference from a normal markdown document is that at the beginning of the markdown document,
you should place the following lines to tell Jekyll to place the page on the website:

```yaml
---
layout: default
title: Page title
author: Your Last name
---
```

Once you commit the file, it will be added to the website, and automatically styled to match the rest of the
website. GitHub provides a [really good guide](https://guides.github.com/features/mastering-markdown/) on how to
write markdown.

For project status updates, place them in the posts folder, make the filename match this style: `yyyy-mm-dd-name.md`
where *name* is the post name, and update the beginning of the file to use `layout:post` If you need to add images
to the post, nest the post in a folder with the same name as it, and place the images in the folder too.

Since Markdown files are just plain text files, any text editor can be used. However, some editors are better than
others, as they have specific markdown support. Some include:

* [GitHub](https://docs.github.com/en/github/managing-files-in-a-repository/adding-a-file-to-a-repository) has a simple
editor and preview system built into it, so you can edit files right on GitHub.com.
* [prose.io](prose.io) is a very simple web-based editor that can open and save Markdown files to GitHub projects.
* [stackedit.io](stackedit.io) is a little bit more advanced web-based editor. Its preview features are better than
prose.io, but configuring it to sync with GitHub is more complicated.
* [Marktext](marktext.app) is an open-source text editor designed specifically for editing Markdown documents. The best
thing about it is that is will display markdown text exactly as it will be displayed on a website.
* [Visual Studio Code](https://code.visualstudio.com/) supports syntax highlighting and page preview for Markdown files.
Additional Markdown features can be added through the use of extensions (such as `markdownlint`, 'unotes', and
`Markdown All in One`. Furthermore, it has git support built in, so you can quickly upload files to the website.

## Local Testing

If you want to test changes that you have made to the site without having to push a commit to GitHub, the
eaisest way is to use Local testing for this website is eaisest with Linux. To test the page locally with Windows,
[install the Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

In Linux:

1. Clone this repository with `git clone https://github.com/Heimdall-Robot/heimdall-robot.github.io.git`.
2. Switch to the pages directory with `cd heimdall-robot.github.io`.
3. Install ruby with `sudo apt install ruby ruby-dev`.
4. Install bundler with `sudo gem install bundler`.
5. Install GitHub Pages bootstrap with `sudo gem install github-pages`.
6. Boostrap the site with `bundle install`.
7. Start serving the website with `bundle exec jekyll serve --incremental`.
8. In your web browser, navigate to `127.0.0.1:4000`.
9. When necessary, update the dependencies with `bundle update`.

While `bundle exec jekyll serve` is running, it will automatically rebuild pages as you make changes to them, so all
you need to do after updating is to reload the page.
The caveat to this is that it will not work on the Windows Subsystem for Linux if the repository was cloned to a
location on the Windows filesystem. There are two fixes for this:

1. Manually rebuild by exiting `bundle exec jekyll serve --incremental` and then re-running it.
2. Move the `heimdall-robot.github.io` directory to a native Linux directory (such as your home folder)
