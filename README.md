# Invoice Hyperledger Application

## Development Environment:
**Go version:** go version go1.11.5 linux/amd64
<br>
**Operating System:** Ubuntu 18.04 LTS

## Setup Network

### Step 1
Create a folder name it **fabric-sample** then create a folder name it **invoice** under **fabric-sample**
then copy all files under **invoice** in this repository then paste it to the directory.
#### Output in the terminal:
**fabric-sample/invoice/ls/**
<br> `app.js`
<br> `enrollAdmin.js`
<br> `package.json`
<br> `registerUser.js`
<br> `startFabric.sh`
 

### Step 2
Create again a folder under **fabric-sample** name it **go**
then copy the file under **go** in this repository then paste it to the directory.
#### Output in the terminal:
**fabric-sample/go/ls/**
<br> `invoice.go`

### Step 3
Open terminal then change directory to **fabric-sample/invoice/** and run the following commands.
<br> `./startFabric.sh`
<br> `npm install`
<br> `node enrollAdmin.js`
<br> `node registerUser.js`
<br> `node app.js`

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

**Goods Received**
<br> http://localhost:3000/invoice
<br> Use the **PUT http request** in this function as we are modifying a data
<br> Select **Form URL Encoded** as a structure.

**Parameters**
- invoiceid
- gr

**Paid to Supplier**
<br> http://localhost:3000/invoice
<br> Use the **PUT http request** in this function as we are modifying a data
<br> Select **Form URL Encoded** as a structure.

**Parameters**
- invoiceid
- ispaid

**Repaid to Bank**
<br> http://localhost:3000/invoice
<br> Use the **PUT http request** in this function as we are modifying a data
<br> Select **Form URL Encoded** as a structure.

**Parameters**
- invoiceid
- repaid
