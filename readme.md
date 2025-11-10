# Minerva Classroom – README

Minerva Classroom is a Quarto website template for math & science lessons, organized by year and subject. It’s based on Quarto and borrows the navigation/sidebar structure of the Network Science Notes site:contentReference[oaicite:3]{index=3}. Each lesson page includes video embeds and LaTeX examples.

## Quickstart

1. **Install Quarto**: Follow the instructions on the [Quarto website](https://quarto.org/docs/get-started/) to install Quarto on your system.
2. **Clone the repository**:  

3. **Preview locally**:  
In the project folder, run `quarto preview`. This will build and serve the site locally (auto-refresh as you edit).
4. **Build the site**:  
Run `quarto render` to generate the site into the `docs/` folder.
5. **Enable GitHub Pages**:  
Commit and push your files, then in your GitHub repo settings enable Pages from the `docs/` folder. The site will be published at `https://<user>.github.io/<repo>/` :contentReference[oaicite:4]{index=4}.

## Adding a New Lesson

- Copy an existing lesson file (e.g. `years/year7/matematik/lesson-01-fractions.qmd`) and rename it (e.g. `lesson-03-newtopic.qmd`).
- Edit the **title** and content in the YAML header of the new file. Update text, math, etc. Replace the dummy `{{< video ... >}}` URL with your own video link.
- Add the new filename to the sidebar navigation in `_quarto.yml`. For example, under the appropriate subject:
```yaml
website:
 sidebar:
   - section: "Matematik"
     href: years/year7/matematik/index.qmd
     contents:
       - years/year7/matematik/lesson-01-fractions.qmd
       - years/year7/matematik/lesson-02-linear-equations.qmd
       - years/year7/matematik/lesson-03-newtopic.qmd   # <-- new lesson
