---
layout: article
title: "Using Static Symbolic Execution to Detect Buffer Overflows"
ref: programming2017
lang: en

pub_authors: "Dudina, I. A. and Belevantsev, A. A."
pub_journal: "Programming and Computer Software, Volume 43, Issue 5, pp 277–288"
pub_year: 2017
pub_keywords: "Buffer overflow, static symbolic execution"
pub_doi: "10.1134/S0361768817050024"

---

Buffer overrun remains one of the main sources of errors and vulnerabilities in the C/C++ source code. To detect such kind of defects, static analysis is widely used. In this paper, we propose a path-sensitive static analysis based on symbolic execution with state merging. For buffers with compile-time-known sizes, we present an interprocedural path- and context-sensitive overrun detection algorithm that finds program points satisfying a proposed error definition. The described
approach was implemented in the Svace static analyzer without significant loss of performance. On Android 5.0.2, these detectors generated 351 warnings, 64% of which were true positives. In addition, we describe a prototype of an intraprocedural heap buffer overflow detector and present an example of a defect found by this detector.
