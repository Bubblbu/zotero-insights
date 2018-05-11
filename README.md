# Zotero Insights

[![eLifeSprint 2018](https://img.shields.io/badge/%23eLifeSprint-2018-blue.svg)](https://github.com/mozilla/global-sprint/issues?q=is%3Aissue+label%3AeLifeSprint)
[![MozSprint 2018](https://img.shields.io/badge/%23MozSprint-2018-orange.svg)](https://mozilla.github.io/global-sprint/)

Extract your highlights and annotations from PDFs stored in Zotero and get insights into your readings and thoughts from the past.

## Use case

> I am a user of Zotero.
I store all my research literature in Zotero collections.
I annotate the PDFs with highlights and comments.
I add notes to many of my Zotero entries.
>
> I want a (basic) text analysis of a specific collection or particular files to aid my literature review: this can be quantitative (word counts and frequencies, e.g.) or qualitative (the context of word appearances and basic sentiment analysis).
>
> I would like the analysis to provide three artefacts:
>
> - A pre-formatted “report” (HTML/PDF)
> - An interactive “report” with “cookbooks” that allows me to tweak the analysis
> - A data dump in a “tidy” format

## Objectives

- [ ] Create Zotero plugin
    - [ ] PDF.js to scan attachments
    - [ ] Export article/annotation content and metadata to a tidy format
- [ ] Platform-independent, interactive reports
    - Python, in Jupyter
    - R Notebooks
- [ ] Works with Binder

## Scope

What do we want to get out of the text, highlights, and comments?

- Basic quant. analysis of full texts.
- See Voyant: https://voyant-tools.org/?corpus=b5abdc236ff751a87090c7aa2ecdf14a
- Analysis of full texts and annotations
    - What are the most frequent categories for individual papers?
    - What are the relevant papers for individual categories?
- Interactively explore articles & annotations
- Show all occurrence of a certain category including quotes from full-texts

## “Tidy” data frame for exporting data

**QUESTION**: How to handle floating annotations? Closest section? Closest paragraph?

|Column|Type|Feature(s)|
|:--|:--|:--|
|ID|numeric|unique, sequential (1…)|
|section #|numeric|sequential (1…)|
|section ID|string / factor [if available]|Abstract / Introduction / etc.|
|Paragraph #|numeric|Within section? Overall document?|
|_**word**_|string / factor|–|
|highlight ID|numeric|Corresponds to sentences/phrases highlighted.|
|is-annotation|binary|–|
|annotation-text|string / dataframe|String can be prepared into own “tidy” data format?|
|code / tag|dataframe|\#hashtag(s)|
|instructions|dataframe|\§instruction(s)|

- Above does NOT include footnotes / endnotes.

## COMING SOON

- [ ] `contributing.md`
- [ ] `code_of_conduct.md`
- [ ] Working examples
