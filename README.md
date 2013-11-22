tabula-extractor
================

[![Build Status](https://travis-ci.org/jazzido/tabula-extractor.png)](https://travis-ci.org/jazzido/tabula-extractor)

Extract tables from PDF files. `tabula-extractor` is the table extraction engine that powers [Tabula](http://tabula.nerdpower.org), now available as a library and command line program.

## Installation

At the moment, `tabula-extractor` only works with JRuby. [Install JRuby](http://jruby.org/getting-started) and run

``
jruby -S gem install tabula-extractor
``


## Usage

```
$ tabula --help
Tabula helps you extract tables from PDFs

Usage:
       tabula [options] <pdf_file>
where [options] are:
     --page, -p <i>:   Page number (default: 1)
     --area, -a <s>:   Portion of the page to analyze (top, left, bottom,
                       right). Example: --area '269.875, 12.75, 790.5, 561'.
                       Default is entire page
   --format, -f <s>:   Output format (CSV,TSV,HTML,JSON) (default: CSV)
  --outfile, -o <s>:   Write output to <file> instead of STDOUT (default: -)
      --version, -v:   Print version and exit
         --help, -h:   Show this message
```

Want to integrate `tabula-extractor` into your own application? We don't have docs yet, but [the tests](test/tests.rb) are a good source of information.

## Scripting examples

`tabula-extractor` is a RubyGem that you can use to programmatically extract tabular data, using the Tabula engine, in your scripts or applications.

## Notes

`tabula-extractor` uses [LSD: a Line Segment Detector](http://www.ipol.im/pub/art/2012/gjmr-lsd/) by Rafael Grompone von Gioi, Jérémie Jakubowicz, Jean-Michel Morel and Gregory Randall.

