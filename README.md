# Pandoc tool for BioDT HTML slides

This repository contains files and instructions for creating HTML slides in the style of the BioDT pptx template, using Pandoc and markdown.
The contents are based on an [existing tool developed by CSC for creating HTML slides](https://github.com/csc-training/csc-env-eff/blob/master/contribute_guide/MD_into_html.md).

For an example slide set, [see this link](https://biodt.github.io/biodt-pandoc/slides/example.html).

# Instructions

## Getting started

1. Install Apptainer/Singularity on your computer. For example, on CentOS:

```
sudo yum install singularity
```

2. Clone this repository.

```
git clone git@github.com:BioDT/biodt-pandoc.git
```

3. Download an Apptainer/Singularity container containing (almost) all the necessary magic. You could, for example, place it in `/usr/bin` (in which case you also need `sudo`).

```
wget https://a3s.fi/pandocTool/pandoc-eurocc.sif
```

## Creating slides

You have two options:

1. Working directly in the repository folder, in which case all is ready to go.
2. Working in a slide folder of your own, in which case you should copy the contents of this repository to that folder.

To create slides:

```
/path/to/pandoc-eurocc.sif -s example.md --theme biodt
```

The resulting HTML file can then be uploaded wherever you'd like, e.g. CSC Allas.
More information on this in a [separate instruction set](https://github.com/csc-training/csc-env-eff/blob/master/contribute_guide/MD_into_html.md#publish-html-files-in-allas).

# Need your slides in PDF?

One easy way is to use [`decktape`](https://github.com/astefanutti/decktape):

```
singularity pull decktape.sif docker://astefanutti/decktape

/path/to/decktape.sif \
-s 2560x1440 \
/path/to/slides.html \
/path/to/output.pdf
```
Just replace the screen resolution with whatever you're using.
If your slides are already hosted on the web, it is also possible to use the html link (e.g. `https://a3s.fi/.../slides.html`), instead of a local file.

# Some development notes

While the template does a fairly good job at reproducing the BioDT Powerpoint template, some issues remain.

- Dates and slide numbers aren't shown, although one could display the date on the title slide.
- Using `{.section}` is currently necessary to get the title positions right in regular slides.
- Some general tweaking could still be done behind the scenes (e.g. the theme wants an image file called section-film.jpg, even if not needed for the BioDT theme specifically).
