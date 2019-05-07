---
layout: default
title: 2-Messy
nav: true
---

# What is Messy Data?

Inconsistent formats, unnecessary white space, extra characters, typos, etc... 
Messy data is the bane of analysis! 
Each column contains exactly the same info:

| 2015-10-14 | $1,000 | ID |
| 10/14/2015 | 1000 | I.D. |
| 10/14/15 | 1,000 | US-ID |
| Oct 14, 2015 | 1000 dollars | idaho |
| Wed, Oct 14th | US$1000 | Idaho, |
| 42291 | $1k | Ihaho |

Multi-valued cells limit ability to manipulate, clean, and use the data:

| “Using OpenRefine by Ruben Verborgh and Max De Wilde, September 2013” | | |
| "University of Idaho, 875 Perimeter Drive, Moscow, ID, 83844, p. 208-885-6111, info@uidaho.edu" | | |

Luckily, Refine provides powerful visualizations and tools to discover these types of data issues, then isolate and fix them.
