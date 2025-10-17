# sum-of-sales-test-001

Publish a single-page site that fetches data.csv from attachments, sums its sales column, sets the title to 'Sales Summary October', displays the total inside #total-sales, and loads Bootstrap 5 from jsdelivr.

## Checks
- js: document.title === 'Sales Summary October'
- js: !!document.querySelector("link[href*='bootstrap']")
- js: Math.abs(parseFloat(document.querySelector("#total-sales").textContent) - 2800) < 0.01

## License
MIT
