---
year: {{date | format("YYYY")}}
tags: research
title: {{ shortTitle }}
authors: {{ authors }}
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

### Notes 

{%- set important = annotations | filterby("comment", "startswith", "important") -%}  
{%- if important.length > 0 %}> [!important] Callouts  
{%- for annotation in important -%}  
{%- if annotation.annotatedText %}  
> - {{annotation.annotatedText | nl2br}}  
{%- endif -%}  
{%- if annotation.imageRelativePath %}  
> - ![[{{annotation.imageRelativePath}}]]  
{%- endif %}  
> [page {{annotation.page}}](file://{{annotation.attachment.path | replace(" ", "%20")}})  
{%- endfor -%}  
{%- endif %}  
{%- if annotations.length %}## Annotations  
{%- endif %}

{%- macro calloutHeader(type, color) -%}  
{%- if type == "highlight" -%}  
<mark style="background-color: {{color}}">Highlight</mark>  
{%- endif -%}{%- if type == "text" -%}  
Note  
{%- endif -%}  
{%- endmacro -%}{%- set annots = annotations | filterby("date", "dateafter", lastExportDate) -%}  
{%- if annots.length > 0 %}  
### Exported: {{exportDate | format("YYYY-MM-DD h:mm a")}}{% for annot in annots -%}  
> {{calloutHeader(annot.type, annot.color)}}  
{%- if annot.annotatedText %}  
> {{annot.annotatedText | nl2br}}  
{%- endif -%}  
{%- if annot.imageRelativePath %}  
> ![[{{annot.imageRelativePath}}]]  
{%- endif %}  
> [page {{annot.page}}](file://{{annot.attachment.path | replace(" ", "%20")}}) [[{{annot.date | format("YYYY-MM-DD#h:mm a")}}]]  
{%- if annot.comment %}  
> - {{annot.comment | nl2br}}  
{% endif %}{% endfor -%}  
{% endif -%}