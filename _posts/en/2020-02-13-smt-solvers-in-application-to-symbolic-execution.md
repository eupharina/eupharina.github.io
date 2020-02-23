---
layout: article
title: "SMT Solvers in Application to Static and Dynamic Symbolic Execution: A Case Study"
ref: isprasopen2019
lang: en

pub_authors: "Nikita Malyshev, Irina Dudina, Daniil Kutz, Alexander Novikov, Sergey Vartanov"
pub_journal: "2019 Ivannikov Ispras Open Conference (ISPRAS), Moscow, Russia, 2019, pp. 9-15."
pub_year: 2019
pub_keywords: "symbolic execution, static analysis, SMT solvers, QF_BV, solver portfolio"
pub_doi: "10.1109/ISPRAS47671.2019.00008"

---

This paper studies the performance and working aspects of SMT solvers on processing formulas acquired during path-sensitive static analysis and dynamic symbolic execution. We review some general patterns of building SMT formulas in the QF_BV logic during analysis and related technical specifics. We also provide the results of comparing different solvers on two sets of requests obtained by Svace static analyzer and Anxiety dynamic symbolic execution tool. It turns out that
Yices2 solver performs the best, although, for Svace, notable part of requests can be done better by other solvers. In return, Yices2 misses some features crucial to top-tier analyzers such as deterministic time limit. A brief attempt at making machine learning based solver portfolio shows that solving time can be enhanced, but requires some serious work on feature selection, while technical difficulties may render it unpractical. For Anxiety we found out that with Yices2
incremental solving is almost always faster (sometimes dozens of times faster) than non-incremental. Moreover, the more queries we solve incrementally, the higher acceleration we get.
