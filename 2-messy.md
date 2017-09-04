---
layout: default
title: 2-Messy
nav: true
---

# What is Messy Data?

Inconsistent formats, unnecessary white space, extra characters, typos, etc... 
Messy data is the bane of analysis! 
Each row contains exactly the same info:

| 2015-10-14 | $1,000 | ID |
| 10/14/2015 | 1000 | I.D. |
| 10/14/15 | 1,000 | US-ID |
| Oct 14, 2015 | 1000 dollars | idaho |
| Wed, Oct 14th | US$1000 | Idaho, |
| 42291 | $1k | Ihaho |

Multivalued cells limit ability to manipulate and use the data:

| “Using OpenRefine by Ruben Verborgh and Max De Wilde, September 2013” | | |
