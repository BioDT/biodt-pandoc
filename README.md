# Pandoc tool for BioDT HTML slides

This repository contains file and instructions for creating HTML slides in the style of the BioDT pptx template, using Pandoc and markdown.
The contents are based on an [existing tool developed by CSC for creating HTML slides](https://github.com/csc-training/csc-env-eff/blob/master/contribute_guide/MD_into_html.md).

# Instructions

## Getting started

1. Install Apptainer/Singularity on your computer. For example, on CentOS:

```
sudo yum install singularity
```

2. Clone this repository.

```
git clone git@github.com:BioDT/biodt-slides.git
```

3. Download an Apptainer/Singularity container containing (almost) all the necessary magic. You could, for example, place it in `/usr/bin` (in which case you also need `sudo`).

```
wget https://a3s.fi/pandocTool/pandoc-eurocc.sif
```

## Creating slides

You have two options:

1. Working directly in the repository folder, in which case all is ready to go
2. Working in a slide folder of your own, in which case you should copy the contents of this repository to that folder.

To create slides:

```
/path/to/pandoc-eurocc.sif -s example.md --theme biodt
```

The resulting HTML file can then be uploaded wherever you'd like, e.g. CSC Allas.
More information on this in a [separate instruction set](https://github.com/csc-training/csc-env-eff/blob/master/contribute_guide/MD_into_html.md#publish-html-files-in-allas).

# Some development notes

While the template does a fairly good job at reproducing the BioDT Powerpoint template, some issues remain.

- Dates and slide numbers aren't shown, although one could display the date on the title slide
- Using `{.section}` is currently necessary to get the title positions right in regular slides
- Some general tweaking could still be done behind the scenes (e.g. the theme wants an image file called section-film.jpg, even if needed for the BioDT theme specifically)
