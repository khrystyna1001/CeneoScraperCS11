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
|opinion | .js_product-review:not(.user-post--highlight) | opinion |
|opinion ID | [data-entry-id] | opinion_id |
|author | .user-post__author-name | author |
|recommendation | .user-post__author-recomendation > em | recommendation |
|number of stars | .user-post__score-count | stars |
|content of opinion | .user.post__text | content |
|list of adventages | .review-feature__item--positive | pros |
|list of disadventages | .review-feature__item--negative | cons |
|for how many helpful | .vote-yes[data-total-vote] | vote_yes |
|for how many unhelpful | .vote-no[data-total-vote] | vote_no |
|publishing date | .user-post__published > time:nth-child(1)[datetime] | published_at |
|purchase date | .user-post__published > time:nth-child(2)[datetime] | purchased_at |