# SC Microservice

SC Microservice is a versatile backend application designed to manage spreadsheet-like cell data using either SQLite or Firebase as its database. This application provides a REST API for creating, updating, reading, and deleting cell data, where each cell contains a unique ID and a formula. It supports resolving formulas that reference other cells, dynamically calculating their values upon retrieval.


## Features
Supports two types of databases: SQLite and Firebase Realtime Database.
CRUD operations for cell data.
Dynamic formula resolution involving references to other cells.
Easy switching between database types using command-line arguments

## Requirements
Python 3.6.8,
Flask,
Requests,
SQLite3,
An active Firebase project and corresponding Firebase Realtime Database URL (for Firebase operations).

## Installation

```bash
pip install Flask requests
```

## Usage
Set up your Firebase Realtime Database and update the FIREBASE_DB_URL in firebase.py with your database URL.

To start the application use the following command:
```python
python3 sc.py -r dbtype
```
Replace dbtype with 'sqlite' or 'firebase'. If you are using firebase, you need to enter the following command beforehand:
```
export FBASE=<Your database name>
```
If the selected data type was 'sqlite', the cells.db file will be overwritten if present in the same directory or a new cells.db file will be created. If the data type is firebase, the database will reset each time before running.
