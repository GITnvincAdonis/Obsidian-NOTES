---
creation date: <% tp.file.creation_date() %>
---

> [!NOTE] [Document Link](https://people.freebsd.org/~lstewart/articles/cpumemory.pdf)
> 

> [!Danger] Worded Table of Contents
> 

### Document Structure

- This document is mostly for software developers. It does not go into enough technical details of the hardware to be useful for hardware-oriented readers. But before we can go into the practical information for developers a lot of groundwork must be laid.

- To that end, the second section describes random-access memory (RAM) in technical detail. This section’s con-tent is nice to know but not absolutely critical to be able to understand the later sections. Appropriate back refer-ences to the section are added in places where the content is required so that the anxious reader could skip most of this section at first.

- The third section goes into a lot of details of CPU cache behavior. Graphs have been used to keep the text from being as dry as it would otherwise be. This content is es-sential for an understanding of the rest of the document. Section 4 describes briefly how virtual memory is imple-mented. This is also required groundwork for the rest. Section 5 goes into a lot of detail about Non Uniform Memory Access (NUMA) systems.

- Section 6 is the central section of this paper. It brings to-gether all the previous sections’ information and gives programmers advice on how to write code which per-forms well in the various situations. The very impatient reader could start with this section and, if necessary, go back to the earlier sections to freshen up the knowledge of the underlying technology.

- Section 7 introduces tools which can help the program-mer do a better job. Even with a complete understanding of the technology it is far from obvious where in a non-trivial software project the problems are. Some tools are necessary.

- In section 8 we finally give an outlook of technology which can be expected in the near future or which might just simply be good to have.

Link to original: [[2025-09-03 Skills to learn for SWE]]