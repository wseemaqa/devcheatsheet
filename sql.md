## Creation & Insertion 
Creating a new table :

```SQL
CREATE TABLE <table name> (
		<column name> <data type>,
		<column name> <data type>,
		.
		.
		.
		<column name> <data type>
);
```

Inserting values into a table :

```SQL
INSERT INTO <table name> VALUES (<val1>,<val2>,....,<valn>);
```
Inserting values in some columns :

```SQL
INSERT INTO <table name>(<column name>,<column name>) 
VALUES (<val1>,<val2>);
```

Data type is important i.e for strings use quotes (ex : ‘python’ instead of python)

Create table from existing table :
```SQL
CREATE TABLE <table name> AS(
	SELECT <column name>,<column name> 
	FROM <table name>
);
```

## Visualization

To get description of a table :

```SQL
DESCRIBE <table name>
```
or (DESC command runs on only the software system// doesn’t run on editors)
```SQL
DESC <table name>
```

## Selection

To get all values :

```SQL
SELECT * FROM <table name> ;
```
To get specific columns :
```SQL
SELECT <column name>, <column name> FROM <table name> ;
```
This can also be achieved by :

```SQL
SELECT ALL <column name> FROM <table name>
```
To get used to specify the number of records in return:

```SQL
SELECT <column_name>
FROM <table name>
WHERE condition
LIMIT number;
```

To get all unique values from a column :

```SQL
SELECT DISTINCT <column name> FROM <table name> ;
```
## Where Conditionals

To select specific rows with a condition :
```SQL
SELECT <column name> 
FROM <table name>
WHERE <condition>
```
