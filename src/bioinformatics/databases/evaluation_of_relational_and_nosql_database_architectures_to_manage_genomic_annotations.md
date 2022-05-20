---
date: June 10, 2021
---

# Evaluation of relational and NoSQL database architectures to manage genomic annotations {.unnumbered}

[Journal of Bimedical Informatics](https://doi.org/10.1016/j.jbi.2016.10.015)

October 31, 2016

> Schulz WL, Nelson BG, Felker DK, Durant TJS, Torres R. Evaluation of
> relational and NoSQL database architectures to manage genomic annotations. J
> Biomed Inform. 2016 Dec;64:288-295. doi: 10.1016/j.jbi.2016.10.015. Epub
> 2016 Oct 31. PMID: [27810480](https://pubmed.ncbi.nlm.nih.gov/27810480).

Document-oriented databases don't use SQL or schemas like SQL databases. They
don't need their structure to be defined in advance and can change over time.
Genomic data is well suited to the document structure because files like VCFs
have extensible fields and can vary. These databases also have faster write
operations and in-memory indexes that improve query efficiency. Some
relational database management systems have the ability to work with both
relational and semi-structured data.

This paper assesses the efficiency of different database types (MongoDB, MySQL,
PostgreSQL)to store and query SNP annotations from dbSNP. They also compared
the efficiency of using a relational model or the binary JSONB data type in
PostgreSQL.

## Results

### Write efficiency

Document-oriented databases offer better performance during write operations
since they do not require any foreign key generation. JSONB objects with
PostgreSQL had faster write performance followed by MongoDB and PostgreSQL.

### Index Creation

The time needed to create an index on the dbSNP data depended on the field used
to create it on. For the JSONB PostgreSQL implementation, the Generalized
Inverted Index method provided the best indexing results on the clinical
significance or the gene name. Since the GIN cannot make a unique index, when
the RSID field was indexed, it was significantly slower than the other
databases.

### Query performance

MongoDB performed best on all but complex queries while MySQL has the lowest.
For the complex query, PostgreSQL with JSONB was the fastest. Overall the
document based models were significantly faster than the relational ones.
