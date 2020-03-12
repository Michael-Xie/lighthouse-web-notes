# ERD
- belongs to a larger realm called UML
	- which describes the layout of the database
## Tool to draw ERD
- draw.io
	- ctrl+enter for new field
	- cardinality of line can be adjusted in options on the right pane

## Cardinality

- relates two tables

### Different types
- 0 to many
- many to many
- 1 to many
- 1 to 1

- a table's cardinality is shown by the crow's feet on the far end of the line
- The Foreign Key is on the many side.

### JOIN table
- many to many can be created by making a new join table that joins the two tables together (table A <one to many> Join <many to one> table B)
- naming is PK, FK1; PK, FK2

## Normal Form
### 1NF
- already have columns and PK specified
- each column and table should contain one value and no repeating groups
- must only have one value and NOT be values separated by commas etc
- no repeating groups means if there are columns like comp1, comp2 ...


