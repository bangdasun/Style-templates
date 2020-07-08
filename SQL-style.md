### Template for SQL Queries

Refer from [How I write SQL code - Marton Trencseni](http://bytepawn.com/how-i-write-sql-code.html?utm_source=wechat_session&utm_medium=social&utm_oi=793431379202441216).

- Keywords in SQL should be all in UPPER case
- Break line for every clause

#### General template

```sql
SELECT
  user_id,
  account_id
FROM 
  customer_info
WHERE
      account_status = 'OPEN'
  AND user_cd = 'PR'
  AND account_credt_dt BETWEEN '2020-06-01' AND '2020-07-01';
```


```sql
SELECT
  cust.user_id,
  cust.account_id,
  purchase.purchase_amount AS amount
FROM 
  customer_info AS cust
LEFT JOIN
  purchase_info AS purchase
ON
  cust.account_id = purchase_info.account_id;
```

#### Format of `CASE WHEN`

```sql
SELECT
  CASE 
    WHEN weekday = 'Monday'  THEN 1
    WHEN weekday = 'Tuesday' THEN 2
    ...
    ELSE 7
  END AS weekday_cd
...
```

### Using `WITH` when results from multiple queries are needed

Much better than sub-queries.

```sql
WITH 
step1 AS (
  /* query 1 */
  SELECT
    ...
  FROM
    ...
  WHERE
    ...
),
step2 AS (
  /* query 2 */
  SELECT
    ...
  FROM
    ...
  LEFT JOIN
    ...
  ON
    ...
)
SELECT
  ...
FROM
  step1
LEFT JOIN 
  step2
ON
  ...
```
