# 15688 Final Project
>This is final project for 15688 @ CMU, 2018, Spring

- - - - 
In the final project, we would like to inspect the relationship between public impressions and the actual strengths of several higher education schools including CMU.
## Scraper
For this part, we would like to use Wikipedia as our main source of data. For each school, we will scrape down their corresponding Wikipedia pages as well as the pages about the famous alumni graduated from the schools. We choose to use alumni information because famous alumni typically contribute a lot to external impressions of a school. 
### Raw Data
#### University
The text data is stored at `data.json` as a dictionary:
```python
{
    'CMU' : {
        'Kathleen_Carley' : "Kathleen M. Carley is an American social scientist ...""
        ...
    }
    ...
    'University_Name':{
        'Person_Name' : "Text"
    }
}
```
It curretly contains data from `['CMU', 'UCLA', 'Stanford', 'Harvard', 'Berklee']`.
#### Disciplines
`disciplines.json`
```python
{
    'Discipline Name' : ['Doc1', 'Doc2', ...]
    'Arts' : ['The arts refers to the theory and physical expression of creativity found in human societies and cultures...']
    ...
}
```
## Analysis 
We treat each Wikipedia page as a document and find its TFIDF or mutual perplexities in the N-gram model so that we can then perform a clustering on the Wikipedia pages. We predict that the clusters of the schools and the alumni will be corresponding to fields of study like science, engineering, literature, art, and so on. The results of this part for each school are then the cluster of the Wikipedia page of the school itself and a radar chart showing the numbers of alumni in each field of study.
### Frequency Analysis

## Visualization
Finally, we will compare the two radar charts across schools. We will find out if schools with similar radar charts of courses have similar charts of alumni and if their Wikipedia pages are in the same cluster. By doing this, we may conclude that the public impression of some school matches its actual strength or that there are prototypes on some school.
 
