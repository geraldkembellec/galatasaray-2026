#Prompt

Create a complete, production-ready HTML5 page from the dataset: https://github.com/geraldkembellec/galatasaray-2026/blob/main/GalatasarayTest26.csv
The generated page must reproduce the spirit and visual quality of the project: https://geraldkembellec.github.io/master-ctm/m2/html-semantique/constance-de-salm.html with the same CSS

while transforming it into a Semantic Web and AI-ready corpus.
## Objective

Build a single-page web application displaying all persons contained in the CSV dataset.
The page must be simultaneously:
* human-readable;
* search-engine friendly;
* schema.org compliant;
* optimized for LLM ingestion;
* optimized for RAG and GraphRAG systems;
* compatible with Linked Open Data principles.

## Dataset Processing
Use : 
``` HTML
  <!DOCTYPE html> <html lang="en">
```
and
``` HTML
<header>
<main>
<footer>
```
Read every row of the CSV file.

Each row represents one historical person.
Generate one semantic card per person.
Extract and display all available fields.

  - ``` <section
    ```  class="person-card"
    ```      itemscope
     ```     itemtype="https://schema.org/Person">
  
If a Wikidata identifier is present, automatically create:  
  - ``` <link itemprop="sameAs" href="https://www.wikidata.org/entity/QXXXXXX">
  - ``` <meta itemprop="identifier" content="Wikidata:QXXXXXX">

Include whenever available:
```html  itemprop="name"
  itemprop="alternateName"
  itemprop="description"
  itemprop="birthDate"
  itemprop="deathDate"
  itemprop="birthPlace"
  itemprop="deathPlace"
  itemprop="nationality"
  itemprop="jobTitle"
  itemprop="image"
  itemprop="sameAs"
  itemprop="identifier"
  itemprop="knowsAbout"
  itemprop="subjectOf"
```
  
