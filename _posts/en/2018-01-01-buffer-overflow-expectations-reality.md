---
layout: article
title: "Buffer Overflow Detection via Static Analysis: Expectations vs. Reality"
ref: syrcose2018
lang: en

pub_authors: "I.A. Dudina"
pub_journal: "Proceedings of the Institute for System Programming, vol. 30, issue 3, pp. 21-30."
pub_year: 2018
pub_keywords: "software error detection; static analysis; buffer overrun"

---

Over the last few decades buffer overflow remains one of the main sources of program errors and vulnerabilities. Among other solutions several static analysis techniques were developed to mitigate such program defects. We analyzed different approaches and tools that address this issue to discern common practices and types of detected errors. Also, we explored some popular sets of synthetic tests (Juliet Test Suite, Toyota ITC benchmark) and set of buggy code snippets extracted
from real applications to define types of defects that a static analyzer is expected to uncover. Both sources are essential to understand the design goals of a production quality static analyzer. Test suites expose a set of features to support that is easy to understand, classify, and check. On the other hand, they don’t provide a real picture of a production code. Inspecting vulnerabilities is useful but provides an exploitation-biased sample. Besides, it does not include defects
eliminated during the development process (probably with the help of some static analyzer). Our research has shown that interprocedural analysis, path-sensitivity and loop handling are essential. An analysis can really benefit from tracking affine relations between variables and modeling C-style strings as a very important case of buffers. Our goal is to use this knowledge to enhance our own buffer overrun detector. Now it can perform interprocedural contextand path-sensitive analysis
to detect buffer overflow mainly for static and stack objects with approximately 65% true positive ratio. We think that promising directions are improving string manipulations handling and combining taint analysis with our approaches.
