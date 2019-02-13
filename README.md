# Invoice Hyperledger Application

## Development Environment:
**Go version:** go version go1.11.5 linux/amd64
**Operating System:** Ubuntu 18.04 LTS

## Setup Network

### Step 1
Create a folder name it **fabric-sample** then create a folder name it **invoice** under **fabric-sample**
then copy all files under **invoice** in this repository then paste it to the directory.
#### Output:
```fabric-sample/invoice/```
<br>   ```app.js```
<br>   ```enrollAdmin.js```
```package.json```
```registerUser.js```
```startFabric.sh```

### Step 2
Create again a folder under **fabric-sample** name it **go**
then copy the file under **go** in this repository then paste it to the directory.
#### Output:
**fabric-sample/go/**
- invoice.go

### Step 3
Open terminal then change directory to **fabric-sample/invoice/**
<br> Then run **./startFabric.sh**
<br> Then run **npm install**
<br> Then run **node enrollAdmin.js**
<br> Then run **node registerUser.js**
<br> Then run **node app.js**

### Step 4
Test the endpoints using **POSTMAN** or **INSOMIA REST Client**.

**Testing Endpoints**
<br> Display All Invoices
<br> http://localhost:3000/
<br> Use the **GET http request** in this function as we are getting data.

**Raise Invoice**
<br> http://localhost:3000/invoice
<br> Use the **POST http request** in this function as we are pushing data
<br> Select **Form URL Encoded** as a structure.

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

**NOTE: gr , ispaid , paidamount , repaid , repaymentamount default values are as follows N , N , 0 , N , 0**
<br> gr = N 
<br> ispaid = N 
<br> paidamount = 0 
<br> repaid = N 
<br> repaymentamount = 0 

**Goods Received**
<br> http://localhost:3000/invoice
<br> Use the **PUT http request** in this function as we are modifying a data
<br> Select **Form URL Encoded** as a structure.

**Parameters**
- invoiceid
- gr

**Bank Payment to Supplier**
<br> http://localhost:3000/invoice
<br> Use the **PUT http request** in this function as we are modifying a data
<br> Select **Form URL Encoded** as a structure.

**Parameters**
- invoiceid
- ispaid

**OEM Repays to Bank**
<br> http://localhost:3000/invoice
<br> Use the **PUT http request** in this function as we are modifying a data
<br> Select **Form URL Encoded** as a structure.

**Parameters**
- invoiceid
- repaid
