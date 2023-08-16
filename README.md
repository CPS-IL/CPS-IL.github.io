# Cyber-Physical Systems Integration Lab 

This repository is for the [homepage of Cyber-Physical Systems Integration Lab](https://cps-il.github.io/).
The previous homepage for this lab is [here](http://publish.illinois.edu/cpsintegrationlab/).

### Contacts

* Lab Director: [Prof. Lui Sha](mailto:lrs@illinois.edu)
* Website Maintainer: [Ayoosh Bansal](mailto:ayooshb2@illinois.edu)

### Acknowledgment

The website uses the amazing template developed by Maruan Al-Shedivat. Check it out at https://github.com/alshedivat/al-folio. Link to [original README](README_al-folio.md).



## Development

### Access

To request write access, send an email to both of the above [contacts](#contacts), including your email id associated with github.

### Installation

Refer to the [original README](README_al-folio.md#installation) for details. An easy option is as follows.

Install [docker](https://docs.docker.com/get-docker/) and [docker-compose](https://docs.docker.com/compose/install/).

```bash
git clone git@github.com:CPS-IL/CPS-IL.github.io.git
cd CPS-IL.github.io
```

### Build and Test

The command below will build and host the website locally. Open http://localhost:8080 from any browser to view. The local url is also displayed on the terminal when the following finishes.

```bash
docker-compose up
```

Once your changes are ready and validated locally, push them to this git repository.


### Checklist

When adding content, it is worth ensuring the following:

* [_bibliography/papers.bib](_bibliography/papers.bib): Add your publications and add/update website specific fields listed below. Current bibliography contains examples for each.
    * abstract - shows expandable paper abstract.
    * bibtex_show - shows expandable bibtex citation.
    * html, pdf, code, poster, slides, website - These create links to the additional material.
    * selected - Show this paper on title page of the website.
    * preview - Provide path to an image/gif that appears to the left of the paper citation.
* [_data/coauthors.yml](_data/coauthors.yml): Used to link author names in the [publication](https://cps-il.github.io/publications/) list.
* [_data/people.yml](_data/people.yml): Data for the [people](https://cps-il.github.io/people/) page.
* [_projects](_projects): Add your projects. Projects are organised based on `category` and can include `related_publications` from  [_bibliography/papers.bib](_bibliography/papers.bib).
* [assets](assets): All files can be added here, however, for large files, e.g., videos, it is preferred to host them elsewhere and add links on this website where appropriate.