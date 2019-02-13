# invoice

## Setup Network

### Step 1
Create a folder name it **fabric-sample** then create a folder name it **invoice** under **fabric-sample**
then copy all files under **invoice** in this repository then paste it to the directory.
#### Output:
**fabric-sample/invoice/**
-------------------- app.js
-------------------- enrollAdmin.js
-------------------- package.json
-------------------- registerUser.js
-------------------- startFabric.sh

### Step 2
Create again a folder under **fabric-sample** name it **go**
then copy the file under go in this repository then paste it to the directory.
#### Output:
**fabric-sample/go/**
---------------- invoice.go

### Step 3
Open terminal then change directory to **fabric-sample/invoice/**
Then run **./startFabric.sh**
Then run **npm install**
Then run **node enrollAdmin.js**
Then run **node registerUser.js**
Then run **node app.js**

### Step 4
Test the endpoints using **POSTMAN** or **INSOMIA REST Client.

**Testing Endpoints**
Display All Invoices
http://localhost:3000/
Use the **GET http request** in this function as we are getting data

**Raise Invoice**
http://localhost:3000/invoice
Use the POST http request in this function as we are pushing data
Select **Form URL Encoded** as a structure

**Parameters**
- invoiceid
- invoicenum
- billedto
- invoicedate
- invoiceamount
- itemdescription
- gr
- ispaid
- paidamount
- repaid
- repaymentamount

**NOTE: gr , ispaid , paidamount , repaid , repaymentamount default values are as follows N , N , 0 , N , 0
gr = N 
ispaid = N 
paidamount = 0 
repaid = N 
repaymentamount = 0 

**Goods Received**
http://localhost:3000/invoice
Use the PUT http request in this function as we are modifying a data
Select **Form URL Encoded** as a structure

**Parameters**
- invoiceid
- gr

**Bank Payment to Supplier**
http://localhost:3000/invoice
Use the PUT http request in this function as we are modifying a data
Select **Form URL Encoded** as a structure

**Parameters**
- invoiceid
- ispaid

**OEM Repays to Bank**
http://localhost:3000/invoice
Use the PUT http request in this function as we are modifying a data
Select **Form URL Encoded** as a structure

**Parameters**
- invoiceid
- repaid
