---
title: Plain Text Data Formats
---

class: center, middle

# Plain Text Data Formats

Database Design

---

# Agenda

1. [Overview](#overview)
1. [Plain text](#plain-text)
1. [Fixed-width text](#fixed-width)
1. [Comma-Separated Values (CSV)](#csv)
1. [JavaScript Object Notation (JSON)](#json)
1. [eXtensible Markup Language (XML)](#xml)
1. [HyperText Markup Language (HTML)](#html)
1. [Conclusions](#conclusions)

---

name: overview

# Overview

---

template: overview

## Intro

There are boundless possibilities when it comes to representing _structured data_ as plain text.

--

In reality, there are just a few common formats that meet most needs.

--

- Comma-Separated Values (CSV)

--

- Javascript Object Notation (JSON)

--

- eXtensible Markup Lanauge (XML)

--

Each of these formats attempts to make data both _human-readable_ and _machine-readable_.

--

We will take a quick look at each.

---

name: plain-text

# Plain text

---

template: plain-text

## Meaning

What do we mean by "_plain text_"?

--

- As you've probably heard, all computer data, including all text, is _ultimately stored as numbers_ in the computer's processor, memory, and storage.

--

- Plain text, for our purposes, means that computer data which contains only numeric codes in the [ASCII](https://en.wikipedia.org/wiki/ASCII) or [Unicode](https://en.wikipedia.org/wiki/Unicode) encoding schemes and nothing else.

--

- ASCII and Unicode offer standardized widely-supported encoding schemes that indicate _which number represents which character_.

--

- For example, the [ASCII standard](https://duckduckgo.com/?q=ascii+chart&t=brave&ia=answer&iax=answer) specifies that an `a` character is represented by the number 97, `b` is 98, `c` is 99, and so on.

--

- So any computer data that contains only a set of these codes, and no other numbers not in these encoding schemes, is "plain text" data.

---

template: plain-text

## Creating

How do we create plain text data?

--

- A _plain text editor_ is an application intended to be used to create plain text files.

--

- Windows' Notepad and Apple's TextEdit are _not good_ plain text editors - both can and will store non-plain-text data into the files they make.

--

- Microsoft Word, Apple Pages, and Google Docs are _not good_ plain text editors.

--

- Almost all computer programming editors and integrated development environments are **good** plain text editors.

---

template: plain-text

## Saving

How to save a file with just plain text in it.

--

- When saving any file, _always include a file extension_ in the filename. This helps the operating system understand what kind of data is in the file and what application it should launch to open it.

--

- A file with _unstructured plain text_ is often saved with the `.txt` extension.

--

- A file with _structured plain text_ is saved with an extension that matches its structure, e.g.:
  - `.csv` for files containing comma-separated-values data
  - `.json` for files containing Javascript Object Notation data
  - `.xml` for files containing eXtensible Markup Language data
  - ... and so on

--

- A filename such as `diabetes_rates_by_state.csv` is a **good filename**, whereas `diabetes_rates_by_state` is not.

---

template: plain-text

## Opening

How do you open a plain text file?

--

- When you double click on a plain text file and it opens in Windows' Notepad or Mac's TextEdit, _quit those applications immediately_ and fix your process!

--

- _Use a good plain text editor_ instead.

--

- Open your good plain text editor and from there open the file using the `File`->`Open...` menu.

--

- It's also possible to _change which application is opened by default_ when you double-click on a file with a certain extension... look it up.

---

template: plain-text

## One more note about file extensions

Annoyingly perhaps, both Windows and Mac OSX hide file extensions by default.

--

- It is **urgent** that you change this setting on your own computer so that file extensions are always visible.

--

- [Research how to do this](https://duckduckgo.com/?q=show+all+file+extensions+mac+and+windows&t=brave&ia=web) for your operating system.

---

name: fixed-width

# Fixed-width text

---

template: fixed-width

## Basic concept

Back in the days when paper ruled, it was useful to print data in nicely-aligned tables that were easy to follow on paper.

--

- Thus was born the fixed-width formatting of text, where data in each column consumes a consistent amount of horizontal space. E.g.:

```bash
Year   Jan  Feb  Mar  Apr  May  Jun  Jul  Aug  Sep  Oct  Nov  Dec    J-D D-N    DJF  MAM  JJA  SON  Year
1880   -29  -18  -11  -20  -12  -23  -21   -9  -16  -23  -20  -23    -19 ***   ****  -14  -18  -20  1880
1881   -16  -17    4    4    2  -20   -7   -3  -14  -21  -22  -11    -10 -11    -18    3  -10  -19  1881
1882    14   15    3  -19  -16  -26  -21   -6  -10  -25  -16  -25    -11 -10      6  -10  -17  -17  1882
```

--

- This example comes from [NASA's records of land and ocean surface temperatures](https://data.giss.nasa.gov/gistemp/tabledata_v3/GLB.Ts+dSST.txt), which are [perhaps shockingly] still published in fixed-width text format.

--

- This data is _very print-friendly_, but _machine-unfriendly_ - it looks good on paper, but is unnecessarily difficult for a computer program to _parse_.

--

---

name: csv

# Comma-Separated Values (CSV)

---

template: csv

## Basic concept

When text is formatted as _comma-separated values_, a series of values is separated by commas*!*

--

- _Line breaks_ separate series of related values.

--

- For example, three lines could be used to represent three different works of nonsense literature:

```csv
Carroll,Lewis,Jabberwocky,1871
Lear,Edward,The Jumblies,1910
Bishop,Elizabeth,The Man-Moth,1946
```

--

- Optionally, the first line of a CSV file can contain _headings_:

```csv
Last name,First name,Title,Year
Carroll,Lewis,Jabberwocky,1871
Lear,Edward,The Jumblies,1910
Bishop,Elizabeth,The Man-Moth,1946
```

---

template: csv

## Consistency

CSV files are used with a _fixed schema_ - a consistent set of fields that are present in each line of the text.

--

- In our example, the _text before the first comma_ is always the author's last name, the following _text before the next comma_ is the author's first name, and so on.

```csv
Carroll,Lewis,Jabberwocky,1871
Lear,Edward,The Jumblies,1910
Bishop,Elizabeth,The Man-Moth,1946
```

--

- Inconsistently-ordered fields would be unusable by a machine and possibly by a human as well - a CSV would never look like this:

```csv
Carroll,Lewis,Jabberwocky,1871
1910,Edward,Lear,The Jumblies
The Man-Moth,1946,Bishop,Elizabeth
```

---

template: csv

## Variation

A variation of the CSV format is the _Tab-Separated Values (TSV)_ format.

--

- An example of three lines of tab-separated values used to represent three different works of nonsense literature (the spaces between values are tabs in this case):

```csv
Carroll    Lewis   Jabberwocky 1871
Lear   Edward  The Jumblies    1910
Bishop Elizabeth   The Man-Moth  1946
```

--

- While _commas are the most common_ separators for this kind of format, tabs, colons `:`, semi-colons `;`, and pipes `|` are not uncommon.

---

name: json

# Javascript Object Notation (JSON)

---

template: json

## A slightly more flexible format

Javascript Object Notation (JSON) is a competitor format to CSV for representing _structured and less structured data_ in text.

--

- For example, the following might be a JSON representation of one work of nonsense literature:

--

```json
{
  "lastName": "Carroll",
  "firstName": "Lewis",
  "title": "Jaberwocky",
  "year": 1871
}
```

--

- Unlike in CSV format, _line breaks, tabs, and spaces are not meaningful_ in JSON format and are used solely for human readability.

--

```json
{
  "last_name": "Carroll",
  "first_name": "Lewis",
  "title": "Jaberwocky",
  "year": 1871
}
```

---

template: json

## Multiple data series

JSON format is valid Javascript programming code. So it may not be a surprise that JSON supports arrays/lists of data series.

--

- For example, three works of nonsense literature might be represented:

```json
[
  {
    "lastName": "Carroll",
    "firstName": "Lewis",
    "title": "Jaberwocky",
    "year": 1871
  },
  {
    "lastName": "Lear",
    "firstName": "Edward",
    "title": "The Jumblies",
    "year": 1910
  },
  {
    "lastName": "Bishop",
    "firstName": "Elizabeth",
    "title": "The Man-Moth",
    "year": 1946
  }
]
```

--

- The _square brackets_ indicate an array. `[ ... ]`

--

- _Commas_ separate the elements of the array. `[ ... , ... , ... ]`

--

- The _line breaks, tabs, and spaces_ are for human-readability only.

---

template: json

## Nesting

JSON can support a hierarchical order of data, also known as _nesting_ of one object within another.

--

- For example, one could nest the _firstName_ and _lastName_ fields within an _author_ field.

```json
{
  "author": {
    "lastName": "Carroll",
    "firstName": "Lewis"
  },
  "title": "Jaberwocky",
  "year": 1871
}
```

--

- This would not be possible with CSV format.

---

template: json

## Less structured data

While JSON, like CSV, is used most commonly for _structured data_, where all series of data have the same fields, this is not a requirement.

--

- For example, some data about three people, with no consistent set of fields:

--

```json
[
  { "name": "Bob", "age": 10 },
  { "last_name": "Lear", "first_name": "Edward", "occupation": "naturalist" },
  { "zodiac": "Libra", "first_name": "Juliette", "favorite_animal": "Koala" }
]
```

---

name: xml

# eXtensible Markup Language (XML)

---

template: xml

## Structured data

Like CSV and JSON, _XML_ can be used to represent _structured data_.

--

```xml
<?xml version="1.0" encoding="UTF-8"?>
<nonsense_works>
    <work>
        <last_name>Carroll</last_name>
        <first_name>Lewis</first_name>
        <title>Jabberwocky</title>
        <year>1871</year>
    </work>
    <work>
        <last_name>Lear</last_name>
        <first_name>Edward</first_name>
        <title>The Jumblies</title>
        <year>1910</year>
    </work>
    <work>
        <last_name>Bishop</last_name>
        <first_name>Elizabeth</first_name>
        <title>The Man-Moth</title>
        <year>1946</year>
    </work>
</nonsense_works>
```

---

template: xml

## Tags and markup

XML tags (code words betweeen `<` and `>` signs) are used to annotate the data and explain its meaning.

--

- For example, the title of each work in the preceeding example is clearly surrounded by `title` _tags_:

```xml
<work>
        <last_name>Bishop</last_name>
        <first_name>Elizabeth</first_name>
        <title>The Man-Moth</title>
        <year>1946</year>
</work>
```

--

- This way of annotating a document with tags is called _markup_.

---

template: xml

## Nesting

As with JSON, XML supports nesting of data, such as placing the `lastName` and `firstName` fields within an `author` field.

--

```xml
    <work>
        <author>
            <last_name>Carroll</last_name>
            <first_name>Lewis</first_name>
        </author>
        <title>Jabberwocky</title>
        <year>1871</year>
    </work>
```

---

template: xml

## For less-structured data

Like, JSON, XML also allows for representing _loosely-structured data_ with inconsistent fields, although this is not common:

--

```xml
<?xml version="1.0" encoding="UTF-8"?>
<people>
    <person>
        <name>Bob</name>
        <age>10</age>
    </person>
    <person>
        <last_name>Lear</last_name>
        <first_name>Edward</first_name>
        <occupation>naturalist</occupation>
    </person>
    <person>
        <zodiac>Libra</zodiac>
        <first_name>Juliette</first_name>
        <favorite_animal>Koala</favorite_animal>
    </person>
</people>
```

---

template: xml

## Similarity to other markup languages

There is a wide variety of subsets of XML for specific purposes.

--

- _Hypertext Markup Language (HTML)_ - the language used for marking up almost all web page content (see [example](#html-example))

-- - The current version, `HTML 5` is not a direct subset of XML, but retains many of the same features as XML.
-- - the previous version, `XHTML` (eXtensible HyperText Markup Language) was a direct subset of XML and followed all XML rules.

--

- _Real Simple Syndication (RSS)_ - used for marking up episodic blog and podcast content (see [example](https://www.cloudwards.net/how-to-set-up-an-rss-feed/))

--

- _Scalable Vector Graphics (SVG)_ - a text-based format for representing vector graphics (see [examples](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Basic_Shapes))

---

name: html

# HyperText Markup Language (HTML)

---

template: html

## Web publishing

Unlike CSV, JSON, and XML, Hypertext Markup Language (HTML) is _not a general-purpose data format_.

--

- HTML is used almost exclusively to define and structure _content published to web pages_.

--

- HTML today is not a sub-set of XML, but _shares much in common with XML_.

--

- Given that web pages are so important today and hold much of the world's data, HTML, despite its obvious flaws, has become _an important plain text data format_.

---

template: html
name: html-example

## Example

An example of a simple HTML document.

```html
<doctype html>
  <html lang="en">
    <head>
      <title>Famous Works of Nonsense Literature</title>
    </head>
    <body>
      <section>
        <h1>Famous Works of Nonsense Literature</h1>
        <article>
          <h2>Jabberwocky</h2>
          <p>by Lewis Carroll<br />1871</p>
        </article>
        <article>
          <h2>The Jumblies</h2>
          <p>by Edward Lear<br />1910</p>
        </article>
        <article>
          <h2>The Man-Moth</h2>
          <p>by Elizabeth Bishop<br />1946</p>
        </article>
      </section>
    </body>
  </html></doctype
>
```

---

template: html

## Challenges

Whereas CSV, JSON, and XML are most often used for packaging data with little consideration to aesthetics, the same cannot be said of HTML.

--

- HTML is _primarily used for publishing web content in a visually-pleasing manner_ (to visually-able humans).

--

- HTML _does not require a consistent repeated data structure_, and often does not have one in practice.

--

- There are drastic differences in the way HTML is written from one web page to the next, making it _difficult to parse_.

---

name: conclusions

# Conclusions

---

template: conclusions

## Comparisons

A few points of comparisons among the various plain text data formats:

--

- CSV, JSON, and XML all support structured data

--

- JSON (and in theory XML, but not in practice) supports loosely structured data

--

- HTML is its own unique creature that is _not going away anytime soon_. We must live with its many flaws, and perhaps even learn to love them.

---

template: conclusions

Thank you. Bye.
