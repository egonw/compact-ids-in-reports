# Using compact identifiers in project reports

Egon Willighagen ([orcid:0000-0001-7542-0286](https://orcid.org/0000-0001-7542-0286))

This document describes how you can improved the FAIR-ness of your project report by using
compact identifiers. Of course, it can be applied to any other document too and has been used
in, for example, journal articles and online documentation already.

Compact identifiers find a balance between compactness in writing and being a persistent, unique,
and global identifier. It "is a string constructed by concatenating a namespace prefix, a separating colon,
and a locally unique identifier (LUI)" [Wimalaratne2018]. For example, for proteins it can
represent the PDB structure [2gc4](https://bioregistry.io/pdb:2gc4) as *pdb:2gc4*.

When the prefixes are defined by community standards, then a compact identifier can be resolved.
There currently two main providers of prefix files [Wimalaratne2018], Identifiers.org [BernalLlinares2021],
and Bioregistry [Hoyt2022]. There match three existing *resolvers* that will take a compact
identifier as part of a resolver URL and redirect to the database with the record matching
that identifier:

* Name-to-Thing (N2T): [https://n2t.net/](https://n2t.net/)
* Identifiers.org: [https://identifiers.org/](https://identifiers.org/)
* Bioregistry.org: [https://bioregistry.io/](https://bioregistry.io/)

Each of these URLs can be extended with a compact identifier. For example, a taxon record
from the NCBI databases or the PDB entry mentioned earlier:

* [https://identifiers.org/taxonomy:9606](https://identifiers.org/taxonomy:9606)
* [https://bioregistry.io/pdb:2gc4](https://bioregistry.io/pdb:2gc4)

## Why use in reports?

Using persistent identifiers is generally accepted as a good practice that benefits science
and has been part of the ideas of FAIR data ([Wilkinson2016]) and of Open Science. Compact
identifiers make it easy to be precise in reports what things the reports talks about: they
are relatively short but very precise at the same time. And that has the benefit that they
are much easier to reuse than labels of things and concepts which intrinsically have a certain
level of uncertainty; a database entry has commonly a very specific meaning.

## Examples uses

The use of compact identifiers can be used in two ways. The simplest is to just put the
compact identifier as plain text in the document, possibly in parentheses:

<ul>
  <i>This report is only about the experimental data of the human (taxonomy:9606) cell lines.</i>
</ul>

Or:

<ul>
  <i>We found that BRCA1 (ensembl:ENSG00000012048) played an important role.</i>
</ul>

Alternatively, you can add a hyperlink with one of the resolvers, for example, Identifiers.org:

<ul>
  <i>We found that BRCA1 (<a href="https://identifiers.org/ensembl:ENSG00000012048">ensembl:ENSG00000012048</a>) played an important role.</i>
</ul>

### Compact identifiers for material identifiers



### Compact identifiers for citation intent annotations

## Conclusion

This document described what the compact identifier is, how it helps linking to online
databases, and how they can be used in written reports as plain text, optionally
hyperlinked with one of the compact identifier resolvers.

# References

* [BernalLlinares2021] Manuel Bernal-Llinares, Javier Ferrer-Gómez, Nick Juty, Carole Goble, Sarala M Wimalaratne, Henning Hermjakob, Identifiers.org: Compact Identifier services in the cloud, Bioinformatics, Volume 37, Issue 12, June 2021, Pages 1781–1782, https://doi.org/10.1093/bioinformatics/btaa864
* [Hoyt2022] Hoyt, C.T., Balk, M., Callahan, T.J. et al. Unifying the identification of biomedical entities with the Bioregistry. Sci Data 9, 714 (2022). https://doi.org/10.1038/s41597-022-01807-3
* [Wilkinson2016] Wilkinson, M., Dumontier, M., Aalbersberg, I. et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 3, 160018 (2016). https://doi.org/10.1038/sdata.2016.18
* [Wimalaratne2018] Wimalaratne, S., Juty, N., Kunze, J. et al. Uniform resolution of compact identifiers for biomedical data. Sci Data 5, 180029 (2018). https://doi.org/10.1038/sdata.2018.29

