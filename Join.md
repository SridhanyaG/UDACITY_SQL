### SELECT orders.*, accounts.* FROM accounts JOIN orders ON accounts.id = orders.account_id;

### SELECT orders.standard_qty, orders.gloss_qty,  orders.poster_qty,  accounts.website,  accounts.primary_poc FROM orders JOIN accounts ON orders.account_id = accounts.id

### SELECT a.primary_poc, w.occurred_at, w.channel, a.name FROM web_events w JOIN accounts a ON w.account_id = a.id WHERE a.name = 'Walmart';

### SELECT r.name region, s.name rep, a.name account FROM sales_reps s JOIN region r ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id ORDER BY a.name;

### SELECT r.name region, a.name account,  o.total_amt_usd/(o.total + 0.01) unit_price FROM region r JOIN sales_reps s ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id JOIN orders o ON o.account_id = a.id;

### SELECT c.countryid, c.countryName, s.stateName FROM Country c JOIN State s ON c.countryid = s.countryid;

### SELECT c.countryid, c.countryName, s.stateName FROM Country c LEFT JOIN State s ON c.countryid = s.countryid;

### SELECT r.name region, s.name rep, a.name account FROM sales_reps s JOIN region r ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id WHERE r.name = 'Midwest' ORDER BY a.name;

### SELECT r.name region, s.name rep, a.name account FROM sales_reps s JOIN region r ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id WHERE r.name = 'Midwest' AND s.name LIKE 'S%' ORDER BY a.name;

### SELECT r.name region, s.name rep, a.name account FROM sales_reps s JOIN region r ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id WHERE r.name = 'Midwest' AND s.name LIKE '% K%' ORDER BY a.name;

### SELECT r.name region, a.name account, o.total_amt_usd/(o.total + 0.01) unit_price FROM region r JOIN sales_reps s ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id JOIN orders o ON o.account_id = a.id WHERE o.standard_qty > 100;

### SELECT r.name region, a.name account, o.total_amt_usd/(o.total + 0.01) unit_price FROM region r JOIN sales_reps s ON s.region_id = r.id JOIN accounts a ON a.sales_rep_id = s.id JOIN orders o ON o.account_id = a.id WHERE o.standard_qty > 100 AND o.poster_qty > 50 ORDER BY unit_price;

### SELECT DISTINCT a.name, w.channel FROM accounts a JOIN web_events w ON a.id = w.account_id WHERE a.id = '1001';

### SELECT o.occurred_at, a.name, o.total, o.total_amt_usd FROM accounts a JOIN orders o ON o.account_id = a.id WHERE o.occurred_at BETWEEN '01-01-2015' AND '01-01-2016' ORDER BY o.occurred_at DESC;





