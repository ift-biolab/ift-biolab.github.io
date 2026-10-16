# Structural Markdown templates

These files are not published. Copy the relevant file into `content/<section>/<new-slug>/index.md`, or copy an existing example bundle directly on github.com. Retain `index.md` and the front matter delimiters. Replace the title, summary, order and every placeholder; add page-local images where appropriate. Use lowercase ASCII filenames with hyphens and no spaces.

Files: `protocol.md`, `equipment.md`, `method.md`, `project.md`. The public example records demonstrate the same structures. Method pages remain prompts until the BioLab team supplies a reviewed method.

Protocols begin **Experimental — incomplete placeholder**. The allowed final status labels are Validated / Experimental / Archived. Keep the visible warning and metadata consistent. A template is never validation evidence. The team must supply the validation process and all scientific, safety and operational details.

For internal links use a relative Markdown source path, for example `../../methods/sample-naming/index.md` from a protocol bundle. Update paths when copying. The build checks content links and images. An optional project URL should be omitted rather than guessed.
