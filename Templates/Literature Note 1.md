---
year: {{date|format("YYYY")}}
title: {{title}}
authors: {{authors}}
tag: literaturenote, zotero
---

### {{title}} {{caseTitle}}

``` ad-info
title: Citation
{{bibliography}}
```

``` ad-info
title: Metadata
- **Title**: {{title}}
- **CiteKey**: {{citekey}}
- **Author**: {{authors}}
- **Year**: {{date}} 
- **Type**: {{itemType}} 
- **DOI**: {{DOI}}
```

```ad-quote
title: Abstract
{{abstractNote}}
```

```ad-abstract
title: Files and Links
- **Ref**: [[@{{citationKey}}]]
- **DOI**: {{DOI}}
- **Url**: {{url}}
- **Uri**: {{uri}}
- **File**: {{file}}
- **Local Library**: [Zotero]({{localLibraryLink}})
- **PDF**: [Zotero]({{pdfZoteroLink}})
```

```ad-note
title: Tags and Collections
- **Keywords**: {{keywordsAll}}
- **Collections**: {{collectionsParent}}
```

### <mark style='background:#4b6584'>Notes</mark> 

