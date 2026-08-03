# REU Website

Made using Academic Pages template -- see more info at https://academicpages.github.io/

# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your public repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

## Running locally

When you are initially working on your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.

## Using Docker

Working from a different OS, or just want to avoid installing dependencies? You can use the provided `Dockerfile` to build a container that will run the site for you if you have [Docker](https://www.docker.com/) installed.

You can build and execute the container by running the following command in the repository:

```bash
chmod -R 777 .
docker compose up
```

You should now be able to access the website from `localhost:4000`.

## Changes for Basic Site

### Already completed in this repo, can be repeated in your own fork of template
1. Remove all files from `_pages` except 404.md, about.md
1. Add new page files to `_pages`: research.md, contact.md
1. Edit `navigation.yml`: declare research and contact as two links in navigation bar
1. Edit `_config.yml`: turn off collections (via `output: false`) and atom feed (`hide: true`)
1. Edit `_includes/footer/custom.html`: remove link to Sitemap (now removed)
1. Remove all existing files from `files`, some files from `images` (keep favicon and manifest.json)
1. Delete: `_data/comments`, `_drafts`, `_portfolio`, `_posts`, `_publications`, `_talks`, `_teaching`, `talkmap*` files and `talkmap` dir, `CONTRIBUTING.md`, and `LICENSE`

### Personalization Steps
1. Fill in personal info in _config.yml
1. Fill in content in about.md, research.md, contact.md
1. Add personal content to `images` and `files`: headshot as profile.png, other images and files

## Troubleshooting
- If styling is not rendering as expected, check the `url` setting in `_config.yml`
- If images and files you added are not loading, check `url` and `baseurl` settings in `_config.yml`
- If you are using a Github Pages Project Site (URL format = https://<owner>.github.io/<repositoryname>; e.g., https://lcjohnso.github.io/REUWebsite) rather than a Github Pages User Site (URL format = https://<owner>.github.io; e.g., https://lcjohnso.github.io), be aware that you'll need to include `{% include base_path %}` and `{{ base_path }}` in all Markdown source files for pages, or use full URLs for the expected hosting location (i.e., /images available at https://lcjohnso.github.io/REUWebsite/images)