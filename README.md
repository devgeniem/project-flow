# Geniem project-flow model

Describes the project model flow used in the various projects by Geniem Oy.

**[Start reading ☞](https://devgeniem.github.io/project-flow/)**

# Editing

The site is hosted via `GitHub Pages`. To make edits to the content, go to the preferred web page on the site and click the edit button on the top right corner. It takes you to the github repository of the project and lets you edit the markdown page directly.

After editing the page, you have to commit the changes. The changes are not merged to the main branch straight away but instead need to be reviewed first by authorized Geniem reviewers.

# For admins

You can add pages locally by cloning the repository and using the included page generator script.

```bash
ruby bin/jekyll-page "{PAGE NAME}" {SECTION NAME} {FILE NAME} {MENU ORDER}
```
Example:
```bash
ruby bin/jekyll-page "Component library" design component-library 5
```

The script makes a new file in the `_pages` folder and links it to a new post in the `_posts` folder with the following content:

```
---
layout: page
title: \"#{title}\"
category: #{category}
date: #{now}
order: #{order}
---
```

# Local development and content reviewing
```
# Start the local jekyll server
bundle exec jekyll serve

# Open the site in your browser
http://localhost:4000/practices/
```

## Sources and more documentation

The idea is based on [10up's best practices -site](https://10up.github.io/Engineering-Best-Practices/).
The site template based on the following great [jekyll template](http://bruth.github.io/jekyll-docs-template). You can find more documentation on the original templates web site and in the code of the project.
