# NLP Utils

## Stopwords
English stopwords list from [Quanteda](https://quanteda.io/reference/stopwords.html) `stopwords`, taken from the SMART information retrieval system (obtained from Lewis, David D., et al. "Rcv1: A new benchmark collection for text categorization research." Journal of machine learning research (2004, 5 April): 361-397.

## Discourse Connector List (DCL)
[The discourse connector list: a multi-genre cross-cultural corpus analysis](https://www.academia.edu/56197786/The_discourse_connector_list_a_multi_genre_cross_cultural_corpus_analysis)
Kalajahi, Seyed Ali Rezvani, Steve Neufeld, and Ain Nadzimah Abdullah. �The Discourse Connector List: a Multi-Genre Cross-Cultural Corpus Analysis.� Text & Talk 37.3 (2017): n. pag. Web.  
[*alternative source*](https://www.eapfoundation.com/vocab/academic/other/dcl/#thedcl)

## Computer Science Academic Vocabulary List (CSAVL)
[When a bug is not a bug: An introduction to the computer science academic vocabulary list.](https://www.semanticscholar.org/paper/When-a-bug-is-not-a-bug%3A-An-introduction-to-the-Roesler/326a8902daa2492165ae5a0e1edf7964775397ef)
Roesler, David. �When a bug is not a bug: An introduction to the computer science academic vocabulary list.� Journal of English for Academic Purposes 54 (2021): 101044.  
[*alternative source*](https://www.eapfoundation.com/vocab/academic/other/csavl/)

## Computer Science Academic Vocabulary List - Specialist (CSAVL-S)
[When a bug is not a bug: An introduction to the computer science academic vocabulary list.](https://www.semanticscholar.org/paper/When-a-bug-is-not-a-bug%3A-An-introduction-to-the-Roesler/326a8902daa2492165ae5a0e1edf7964775397ef)
Roesler, David. �When a bug is not a bug: An introduction to the computer science academic vocabulary list.� Journal of English for Academic Purposes 54 (2021): 101044.  
[*alternative source*](https://www.eapfoundation.com/vocab/academic/other/csavl/)

## Computer Science Word List (CSWL)
[A Computer Science Word List](https://www.baleap.org/wp-content/uploads/2016/03/Daniel-Minshall.pdf)
Minshall, Daniel E. "A Computer Science Word List." Masters thesis, Swansea University, 2013.  
[*alternative source*](https://www.eapfoundation.com/vocab/academic/other/csavl/)  


## Computer Science Multi-Word List (CSMWL)
[A Computer Science Word List](https://www.baleap.org/wp-content/uploads/2016/03/Daniel-Minshall.pdf)
Minshall, Daniel E. "A Computer Science Word List." Masters thesis, Swansea University, 2013.  
[*alternative source*](https://www.eapfoundation.com/vocab/academic/other/csavl/)

## Stack Exchange Tags List
[Query Editor](https://data.stackexchange.com/stackoverflow/query/edit/1602765)
Query:
```SQL
select 
  e.id,
  t.tagName,
  t.Count as tagCount,
  count(t.tagName) synonymsCount,
  string_agg(TagSynonyms.SourceTagName, '___') as synonyms,
  e.body as 'Excerpt'
from tags t
left join Posts e
  on t.ExcerptPostId = e.Id
left join TagSynonyms 
  on TagSynonyms.TargetTagName = t.tagName
group by e.id, t.tagName, t.Count, e.body
order by t.Count desc
```
