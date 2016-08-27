# Schema Information

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
username        | string    | not null, indexed, unique
email           | string    | not null, indexed, unique
password_digest | string    | not null
session_token   | string    | not null, indexed, unique

## applications
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
company     | string    | not null
job_title   | string    | not null
progress    | string    | not null, default: 'application'
user_id     | integer   | not null, foreign key (references users), indexed

## events
column name      | data type | details
-----------------|-----------|-----------------------
id               | integer   | not null, primary key
title            | string    | not null
date_time        | string    | not null
notes            | string    |
application_id   | string    | not null, foreign key (references application), indexed

## contacts
column name      | data type | details
-----------------|-----------|-----------------------
id               | integer   | not null, primary key
fname            | string    | not null
lname            | string    |
phone            | string    |
email            | string    |
linkedin         | string    |
address          | string    |
application_id   | string    | not null, foreign key (references application), indexed
