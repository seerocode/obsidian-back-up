---
year: {%- if date -%} ({{date | format("YYYY")}}) {%- endif -%}
tags: research
title: {{shortTitle}}
authors: {{authors}}
---

### {{title}} {{caseTitle}}

``` ad-info
title: Metadata
- **Title**: {{title}}
- **CiteKey**: [@{{citekey}}]
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
{% for annotation in annotations -%}{%- if annotation.annotatedText -%}{% if 'Red' in annotation.colorCategory %} 
##### {{annotation.annotatedText | escape }}{% else %}
<mark class="customZot-{% if annotation.color %}{{annotation.colorCategory}} {% endif %}">{{annotation.annotatedText | escape }}</mark> ([{{annotation.page}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.page}}&annotation={{annotation.id}}))

{% endif %}{%- endif %} {% if annotation.imageRelativePath %} ![[{{annotation.imageRelativePath}}]]{% endif %}{% if annotation.comment %} 
>{{annotation.comment}}
{% endif %}{% endfor -%}