# Single-Table-Inheritance-VS-Multiple-Table-Inheritance

## What is Single Table Inheritance ?

**STI** is a database design pattern where a single table stores different types of records.

These records have a subset of shared columns and another column that instructs the application which object that record should be represented by.

Even though this is the most common pattern, yet it has its downsides:

- **wasted space**: due to the fact that STI collects both common and non-common columns/attributes of types we'll definitely suffer from null values.

- **size**: **STI** gathers all similar types in a single table which results in a huge table size.

After knowing the cons, there's an up side to it, which is:

- all the data is in a single place, making it easier to write queries, easier to make modifications , and avoiding joins.

## What is Multiple Table Inheritance ?

**MTI** is a pattern where we try to mirror inheritance in OOP, where common attributes are represented as columns (obviously) in a parent table, and non-common attributes are stored in different tables, the later tables also have a **foreign key** to reference the row in the parent table.

the biggest disadvantage is that queries will take longer to load, due to *joins*s.