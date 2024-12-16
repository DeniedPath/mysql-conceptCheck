# MySQL Data Types Examples

This repository contains various SQL scripts demonstrating the use of different MySQL data types, including how to create tables, insert data, and perform queries. Each section focuses on a specific data type, providing practical examples for understanding their usage.

## Table of Contents
- [Storing Large Text Data](#storing-large-text-data)
- [Storing & Querying JSON](#storing--querying-json)
- [Data Types: Dates & Times](#data-types-dates--times)
- [Data Types: Float Points](#data-types-float-points)
- [Data Types: Integers](#data-types-integers)
- [Data Types: Strings, CHAR & VARCHAR](#data-types-strings-char--varchar)
- [Combining Numbers & Dates](#combining-numbers--dates)
- [Data Type: Numeric](#data-type-numeric)

## Storing Large Text Data

This section demonstrates how to create a table for storing large text data using the `MEDIUMTEXT` type.

CREATE TABLE large_text_data (
id INT AUTO_INCREMENT PRIMARY KEY,
title VARCHAR(255),
content MEDIUMTEXT,
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


### Key Points:
- `MEDIUMTEXT` can store up to 16MB of text.
- Suitable for articles or long descriptions.

## Storing & Querying JSON

This section shows how to create a table for storing JSON data and how to query it.

CREATE TABLE json_data (
id INT AUTO_INCREMENT PRIMARY KEY,
data JSON,
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


### Key Points:
- The `JSON` data type allows for storing valid JSON documents.
- MySQL provides functions and operators to query JSON data effectively.

## Data Types: Dates & Times

This section covers how to store date and time values in MySQL.

CREATE TABLE date_time_example (
id INT AUTO_INCREMENT PRIMARY KEY,
event_date DATE,
event_time TIME,
event_datetime DATETIME,
event_timestamp TIMESTAMP,
event_year YEAR
);


### Key Points:
- Various types like `DATE`, `TIME`, `DATETIME`, and `TIMESTAMP` are available.
- Use functions like `DATEDIFF()` to manipulate date values.

## Data Types: Float Points

This section demonstrates how to create a table for storing floating-point numbers.

CREATE TABLE float_point_example (
id INT AUTO_INCREMENT PRIMARY KEY,
float_value FLOAT(7, 4),
double_value DOUBLE(16, 8),
decimal_value DECIMAL(10, 4)
);


### Key Points:
- Use `FLOAT` and `DOUBLE` for approximate values.
- Use `DECIMAL` for exact precision, especially in financial applications.

## Data Types: Integers

This section illustrates how to store integer values in MySQL.

CREATE TABLE integer_example (
id INT AUTO_INCREMENT PRIMARY KEY,
small_int_value SMALLINT,
medium_int_value MEDIUMINT,
int_value INT,
big_int_value BIGINT,
tiny_int_value TINYINT
);


### Key Points:
- Integer types range from `TINYINT` (1 byte) to `BIGINT` (8 bytes).
- Choose the appropriate type based on the expected range of values.

## Data Types: Strings, CHAR & VARCHAR

This section explains the differences between `CHAR` and `VARCHAR`.

CREATE TABLE string_example (
id INT AUTO_INCREMENT PRIMARY KEY,
char_value CHAR(10),
varchar_value VARCHAR(255)
);


### Key Points:
- `CHAR` is fixed-length; it pads shorter strings with spaces.
- `VARCHAR` is variable-length; it only uses as much space as needed.

## Combining Numbers & Dates

This section shows how to combine numeric values with dates in a table.

CREATE TABLE number_date_example (
id INT AUTO_INCREMENT PRIMARY KEY,
event_date DATE,
attendees INT,
ticket_price DECIMAL(10, 2),
total_revenue DECIMAL(10, 2)
);
text


### Key Points:
- You can perform calculations involving both numeric and date values.
- Useful for tracking events and related financial metrics.

## Data Type: Numeric

This section covers various numeric data types in MySQL.

CREATE TABLE numeric_example (
id INT AUTO_INCREMENT PRIMARY KEY,
small_num SMALLINT,
medium_num MEDIUMINT,
int_num INT,
big_num BIGINT,
float_num FLOAT(7, 4),
double_num DOUBLE(16, 8),
decimal_num DECIMAL(10, 2)
);


### Key Points:
- Numeric types include integers and floating-point numbers.
- Choose the appropriate type based on precision and range requirements.

---

Feel free to explore each section for detailed examples and explanations!
