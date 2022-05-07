# Design principles for data intensive applications
Replication means keeping a copy of the same data on multiple machines that are connected via a network. As discussed in the introduction to Part II, there are several
reasons why you might want to replicate data:
- To keep data geographically close to your users (and thus reduce latency)
- To allow the system to continue working even if some of its parts have failed(and thus increase availability)
- To scale out the number of machines that can serve read queries (and thus increase read throughput)

# SQL
Order of execution in a SQL query:
- FROM [MyTable]
- ON [MyCondition]
- JOIN [MyJoinedTable]
- WHERE [...]
- GROUP BY [...]
- HAVING [...]
- SELECT [...]
- ORDER BY [...]
- LIMIT

- JOIN/INNER JOIN : Fetch all rows which match the join criteria
- LEFT JOIN: INNER JOIN + all other records from table on left of join
- RIGHT JOIN: INNER JOIN + all other records from table on right of join
- Multiple JOINS: Join initiated from left and progressively joins the result with next table

https://www.sqlshack.com/learn-sql-sql-query-practice/