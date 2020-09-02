# Heimdall Website

This is the source repository for the project website. Whenever a change is made to this repository's master branch,
it willl automatically update [heimdall-robot.github.io](heimdall-robot.github.io).

## How it works

All of the pages in the website are written in [Markdown](https://en.wikipedia.org/wiki/Markdown). When a new commit is
made to the repository, [GitHub Pages](pages.github.com) uses the [Jekyll](https://jekyllrb.com/) static site generator
to generate a complete set of HTML and CSS files, which are then published to
[heimdall-robot.github.io](heimdall-robot.github.io)

## Adding pages

To add a page to the website, simply create a new [Markdown](https://en.wikipedia.org/wiki/Markdown) file in this
repository. On the next commit, it will be added to the website, and automatically styled to match the rest of the
website.

For project status updates, place them in the posts folder, and make the filename match this style: `yyyy-mm-dd-name.md`
where *name* is the post name. If you need to add images to the post, nest the post in a folder with the same name as
it, and place the images in the folder too.

Since Markdown files are just plain text files, any text editor can be used. However, some editors are better than
others, as they have specific markdown support. Some include:

* [Visual Studio Code](https://code.visualstudio.com/) supports syntax highlighting and page preview for Markdown files.
Additional Markdown features can be added through the use of extensions (such as `markdownlint`, 'unotes', and
`Markdown All in One`. Furthermore, it has git support built in, so you can quickly upload files to the website.
* [Marktext](marktext.app) is an open-source text editor designed specifically for editing Markdown documents. The best
thing about it is that is will display markdown text exactly as it will be displayed on a website.
* [prose.io](prose.io) is a very simple web-based editor that can open and save Markdown files to GitHub projects.
* [stackedit.io](stackedit.io) is a little bit more advanced web-based editor. Its preview features are better than
prose.io, but configuring it to sync with GitHub is more complicated.

## Changing the theme:

## Local Testing

If you want to test changes that you have made to the site without having to push a commit to GitHub, the
eaisest way is to use Local testing for this website is eaisest with Linux. To test the page locally with Windows, install the Windows
Subsystem for Linux on Windows.

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
