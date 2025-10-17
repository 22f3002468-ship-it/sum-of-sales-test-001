# sum-of-sales-test-001

Enhance the site by adding a Bootstrap table #product-sales that lists each product with its total sales and keeps #total-sales accurate. Introduce a currency select #currency-picker that converts the computed total using rates.json. Add filtering by region via #region-filter and update #total-sales accordingly.

## Checks
- js: document.querySelectorAll("#product-sales tbody tr").length >= 1
- js: (() => { const rows = [...document.querySelectorAll("#product-sales tbody tr td:last-child")]; const sum = rows.reduce((acc, cell) => acc + parseFloat(cell.textContent), 0); return Math.abs(sum - 2800) < 0.01; })()
- js: !!document.querySelector("#currency-picker option[value='USD']")
- js: !!document.querySelector("#total-currency")
- js: document.querySelector("#region-filter").tagName === "SELECT"
- js: document.querySelector("#total-sales").dataset.region !== undefined

## License
MIT
