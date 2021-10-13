1.Create an index that will enable a user to pull orders for ‘1990-10-03’ out of the Orders table quickly.


```SQL

D5_56760>EXPLAIN FORMAT=JSON
        SELECT * FROM ORDERS WHERE odate='1990-10-03';
    -- "cost_info": {
    --   "query_cost": "1.25"
    -- }

D5_56760>CREATE INDEX idx_orders_date ON ORDERS(odate);
Query OK, 0 rows affected (0.59 sec)
Records: 0  Duplicates: 0  Warnings: 0

D5_56760>EXPLAIN FORMAT=JSON
        SELECT * FROM ORDERS WHERE odate='1990-10-03';
-- "cost_info": {
--       "query_cost": "1.00"
--     },


````


2. If the Orders table has already been created, how can you force the onum field to be unique (assume all current values are unique)?

```SQL


```

