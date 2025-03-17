# CeneoScraperCS11
https://www.ceneo.pl/84514582#tab=reviews

## Ceneo scraping algorithm
1. analysis of the structure of the webpage
2. send http request to access page with opinions
3. check the status code of http response
4. parse the html code of first page with opinions
5. extract required data from parsed code
6. if there are more pages, move to the next page and repeat steps 2-6 for each one of them
7. save extracted data

## Analysis of the structure of the webpage
|Component|Selector|Variable|
|---------|--------|--------|
|opinion ID | id | |
|author | class | |
|recommendation | class | |
|number of stars | element | |
|content of opinion | element | |
|list of adventages | class | |
|list of disadventages | class | |
|for how many helpful | class | |
|for how many unhelpful | class | |
|publishing date | id | |
|purchase date | id | |