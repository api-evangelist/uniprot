# UniProt

Universal protein database providing free, open access to protein sequences, functional annotations, cross-references, and taxonomic information via a REST API and SPARQL endpoint.

**Base URL:** https://rest.uniprot.org  
**Documentation:** https://www.uniprot.org/help/api  
**License:** CC BY 4.0  
**Authentication:** None required  

## APIs

| API | Base URL | Description |
|-----|----------|-------------|
| UniProtKB REST API | https://rest.uniprot.org/uniprotkb | Search and retrieve reviewed (Swiss-Prot) and unreviewed (TrEMBL) protein entries |
| UniRef REST API | https://rest.uniprot.org/uniref | Access sequence cluster databases (UniRef100/90/50) |
| UniParc REST API | https://rest.uniprot.org/uniparc | Non-redundant archive of all public protein sequences |
| Proteomes REST API | https://rest.uniprot.org/proteomes | Complete protein sets from fully sequenced organisms |
| ID Mapping REST API | https://rest.uniprot.org/idmapping | Map between UniProt accessions and 150+ external database IDs |
| UniProt SPARQL | https://sparql.uniprot.org/sparql | SPARQL 1.1 endpoint over 232B+ RDF triples |
| EBI Proteins REST API | https://www.ebi.ac.uk/proteins/api | Protein annotations plus large-scale variation and proteomics data |

## Key Endpoints (UniProtKB)

```
GET /uniprotkb/search?query={query}&format={format}&size={size}
GET /uniprotkb/{accession}
GET /uniprotkb/{accession}.fasta
GET /uniprotkb/{accession}/publications
GET /uniprotkb/stream?query={query}&format={format}
```

## Formats Supported

`json`, `fasta`, `tsv`, `xlsx`, `xml`, `rdf`, `txt`, `list`, `gff`

## Rate Limits

- **UniProt REST API:** No hard published limit; use pagination/streaming for bulk access
- **EBI Proteins API:** 200 requests/second/user
- **SPARQL endpoint:** 45-minute query timeout

## Pricing

Free. No API key required. No registration required.

## License

All UniProt data is available under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.

## Consortium

UniProt is maintained by:
- [EMBL-EBI](https://www.ebi.ac.uk/) — European Bioinformatics Institute
- [SIB](https://www.sib.swiss/) — Swiss Institute of Bioinformatics
- [PIR](https://proteininformationresource.org/) — Protein Information Resource
