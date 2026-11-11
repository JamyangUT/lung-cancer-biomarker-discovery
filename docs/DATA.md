# Referenced Data Sources

The project documents name the ten accessions below. GEO assay types, platforms, and listed sample counts were checked against the public series records on November 12, 2026.

**These are referenced accessions, not a verified manifest of the final discovery or test cohorts.** The documents repeatedly describe an eight-dataset analysis without consistently identifying its exact membership. Listed sample counts refer to GEO records and do not establish the number of independent subjects or analyzed samples.

| GEO accession | Assay type | Platform | Listed GEO samples |
| --- | --- | --- | ---: |
| [GSE268175](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE268175) | High-throughput expression sequencing | GPL16791 | 67 |
| [GSE7670](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE7670) | Expression microarray | GPL96 | 66 |
| [GSE43458](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE43458) | Expression microarray | GPL6244 | 110 |
| [GSE19804](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE19804) | Expression microarray | GPL570 | 120 |
| [GSE40791](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE40791) | Expression microarray | GPL570 | 194 |
| [GSE18842](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE18842) | Expression microarray | GPL570 | 91 |
| [GSE32863](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE32863) | Expression microarray | GPL6884 | 116 |
| [GSE21933](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE21933) | Expression microarray | GPL6254 | 42 |
| [GSE19188](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE19188) | Expression microarray | GPL570 | 156 |
| [GSE10072](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE10072) | Expression microarray | GPL96 | 107 |

## Important interpretation details

Most referenced datasets are microarrays. Accordingly, the project is described as gene-expression analysis rather than as a uniformly RNA-Seq-based study.

Series matrices may contain processed expression measurements, rather than raw RNA-Seq counts. Platform-specific normalization and gene/probe mapping need to be established before reconstructing a joint matrix.

GSE10072's record describes 107 final expression values from 58 tumor and 49 non-tumor tissues. That matches the matrix size stated in the project documents, but size agreement alone cannot prove that the project's final matrix came exclusively from this accession.

Original raw/processed datasets are hosted by GEO and are not redistributed in this repository.
