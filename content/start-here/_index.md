---
title: "Start Here"
description: "Read the site conventions, publication limits and editing guide."
weight: 10
---

## Read before using a resource

**Equipment and Materials contain the first inventory records.** Confirmed purchase records and reported items awaiting verification are labelled separately; neither is a live stock or access statement. Other sections still include placeholder/example records. These do not supply usable procedures, equipment instructions, training requirements or safety rules. The BioLab team must supply and review those details.

Protocol records use three labels: **Validated / Experimental / Archived**. A label alone is not evidence of validation. Review the version, last-tested date, responsible person and supporting documentation. The example protocol is **Experimental — incomplete placeholder**.

## Find information

- [Protocols](../protocols/_index.md): structured protocol records.
- [Equipment](../equipment/_index.md): confirmed equipment purchase records and documentation.
- [Materials](../materials/_index.md): confirmed materials/consumables and a separate reported chemical inventory.
- [Methods](../methods/_index.md): prompts for reasoning and documentation.
- [Courses](../courses/_index.md): learning material and assignments.
- [Projects](../projects/_index.md) and [Students](../students/_index.md): manually maintained overviews and external links.

Use the sidebar, breadcrumbs or search to move around. Student sites have their own **Project / Experiments / Notebook** structure; weekly entries belong inside Notebook.

## Edit documentation on GitHub

1. Open the page toolbar's **Edit this page on GitHub** link. On a small screen it may be under **More**. Before publication, the future repository link is not yet available.
2. Edit the Markdown in `content/`, retain the front matter between `---` lines, and preview the change. English and French prose are both supported; interface labels stay English.
3. Upload images beside the page's `index.md`, using **Add file → Upload files** in that folder. Reference them with `![Meaningful description](image-name.jpg)`.
4. Commit the change (or open a pull request if repository rules require it). Check **Actions → Build and deploy Pages** and wait for both build and deploy to succeed.

To add a record, copy an example page bundle into a new lowercase, hyphenated folder in `content/`. Keep the filename `index.md`, replace the title and placeholders, and update any relative links. Copy its images only if still relevant. No Hugo or CSS edits are needed. Administrators can also start from the structural files in `templates/`; see the repository README.

Prefer JPEG/WebP photographs and SVG/PNG diagrams. Give images descriptive alt text and a caption. Avoid video, raw camera dumps and very large files. There is no Git LFS setup.

> [!WARNING] Public publication
> Repositories and published pages are public. Do not commit passwords, personal data, confidential partner information, unpublished proprietary protocols or restricted research data. Publish student names and links only after the team has confirmed the appropriate information for public release.

## Missing or broken information

Contact the responsible maintainer **[to be supplied by the BioLab team]**. If a build fails, inspect its Actions log and contact an administrator rather than changing technical configuration.
