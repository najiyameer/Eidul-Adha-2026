<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Naimi Qurbani Invoice</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:#dfe5e1;
    font-family:'Poppins',sans-serif;
    padding:20px;
}

/* MAIN */

.invoice{
    width:630px;
    background:white;
    margin:auto;
    border-radius:12px;
    padding:20px;
    position:relative;
    overflow:hidden;
}

/* WATERMARK */

.watermark{
    position:absolute;
    width:260px;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    opacity:0.04;
    z-index:0;
}

/* HEADER */

.header{
    display:flex;
    justify-content:space-between;
    align-items:flex-start;
    position:relative;
    z-index:2;
}

.left-header{
    display:flex;
    gap:10px;
}

.logo{
    width:45px;
    height:45px;
}

.title h1{
    font-size:18px;
    font-weight:800;
    color:#003f2f;
}

.title p{
    color:#c99820;
    font-size:12px;
}

.right-header{
    text-align:right;
}

.right-header h2{
    font-size:14px;
    margin-bottom:2px;
}

.right-header p{
    font-size:10px;
}

/* LINE */

.gold-line{
    height:2px;
    width:100%;
    background:#c99820;
    margin:12px 0;
}

/* TOP SECTION */

.top-section{
    display:flex;
    justify-content:space-between;
    gap:20px;
    position:relative;
    z-index:2;
}

.customer{
    width:65%;
}

.details{
    width:35%;
}

/* INPUTS */

.input-box{
    margin-bottom:10px;
}

.input-box input,
.input-box textarea{
    width:100%;
    border:none;
    border-bottom:2px solid #d9d9d9;
    padding:6px 0;
    font-size:12px;
    outline:none;
    background:transparent;
    font-family:'Poppins',sans-serif;
}

.input-box textarea{
    resize:none;
    height:45px;
}

.input-box input:focus,
.input-box textarea:focus{
    border-color:#c99820;
}

/* DETAIL */

.small-label{
    color:#d62828;
    font-size:8px;
    font-weight:700;
    margin-top:6px;
}

.detail-box{
    border-bottom:2px solid #c99820;
    margin-bottom:8px;
    padding-bottom:3px;
}

.detail-box input{
    border:none;
    outline:none;
    width:100%;
    font-size:11px;
    background:transparent;
    font-family:'Poppins',sans-serif;
}

/* DATE + TIME */

input[type="date"],
input[type="time"]{
    cursor:pointer;
}

/* DONATION */

.donation-box{
    margin-top:12px;
}

.donation-label{
    display:flex;
    align-items:center;
    gap:8px;
    font-size:11px;
    font-weight:500;
    color:#003f2f;
    cursor:pointer;
}

.donation-label input{
    width:14px;
    height:14px;
    cursor:pointer;
}

/* TABLE */

table{
    width:100%;
    border-collapse:collapse;
    margin-top:10px;
    position:relative;
    z-index:2;
    table-layout:fixed;
}

th{
    background:#003f2f;
    color:white;
    padding:7px;
    font-size:11px;
}

td{
    border-bottom:1px solid #ddd;
    padding:5px;
    text-align:center;
    font-size:11px;
    overflow:hidden;
}
/* INPUT TABLE */

.share-input,
.name-input{
    width:100%;
    max-width:100%;
    border:none;
    background:transparent;
    outline:none;
    font-size:11px;
    font-family:'Poppins',sans-serif;
    display:block;
    box-sizing:border-box;
}
    
/* REMOVE */

.remove-btn{
    background:none;
    border:none;
    color:#d62828;
    font-size:16px;
    cursor:pointer;
}

/* ADD BUTTON */

.add-btn{
    margin-top:10px;
    background:#003f2f;
    color:white;
    border:none;
    padding:8px 14px;
    border-radius:8px;
    font-size:11px;
    cursor:pointer;
}

/* TOTAL */

.total{
    text-align:right;
    margin-top:10px;
    font-size:18px;
    font-weight:800;
    color:#003f2f;
    position:relative;
    z-index:2;
}

/* BOTTOM BUTTONS */

.bottom-buttons{
    width:630px;
    margin:15px auto 0;
    display:flex;
    gap:10px;
}

.download-btn,
.whatsapp-btn{
    border:none;
    color:white;
    padding:12px 18px;
    border-radius:10px;
    cursor:pointer;
    font-weight:700;
    font-size:13px;
}

.download-btn{
    background:#d4a017;
}

.whatsapp-btn{
    background:#25D366;
}

/* PRINT */

@media print{

    @page{
        size:A4 portrait;
        margin:5mm;
    }

    body{
        background:white;
        padding:0;
    }

    .invoice{
        width:100%;
        border-radius:0;
        box-shadow:none;
        padding:10px;
    }

    .bottom-buttons,
    .add-btn,
    .remove-btn{
        display:none;
    }

    th{
        background:#003f2f !important;
        color:white !important;
        -webkit-print-color-adjust:exact;
        print-color-adjust:exact;
    }

    .gold-line{
        background:#c99820 !important;
        -webkit-print-color-adjust:exact;
        print-color-adjust:exact;
    }

}

/* MOBILE */

@media(max-width:700px){

table{
    width:100%;
    table-layout:auto;
}

td,th{
    white-space:normal;
}

.share-input,
.name-input{
    width:100%;
    min-width:0;
}

.invoice{
    width:100%;
}

.bottom-buttons{
    width:100%;
}

.top-section{
    flex-direction:column;
}

.customer,
.details{
    width:100%;
}

.header{
    flex-direction:column;
    gap:10px;
}

.right-header{
    text-align:left;
}

}

</style>
</head>

<body>

<div class="invoice">

<img src="logo.png" class="watermark">

<!-- HEADER -->

<div class="header">

<div class="left-header">

<img src="Logo.jpeg" class="logo">

<div class="title">
<h1>NAIMI QURBANI CENTRE</h1>
<p>Buffalo Share Invoice</p>
</div>

</div>

<div class="right-header">
<h2>Syed Mahfooz Alam</h2>
<p>+91 9412475675</p>
<p>mnaimi550@gmail.com</p>
<p>Jamia Naimia, Moradabad</p>
</div>

</div>

<div class="gold-line"></div>

<!-- TOP -->

<div class="top-section">

<div class="customer">

<div class="input-box">
<input type="text" id="customerName" placeholder="Customer Name">
</div>

<div class="input-box">
<input type="text" id="phone" placeholder="Phone Number">
</div>

<div class="input-box">
<textarea id="address" placeholder="Address"></textarea>
</div>

</div>

<div class="details">

<div class="small-label">
REPORTING TIME
</div>

<div class="detail-box">
<input type="time" value="11:00">
</div>

<div class="small-label">
    DATE OF BOOKING
    </div>
    
    <div class="detail-box">
    <input type="date" id="bookingDate">
    </div>

<div class="small-label">
DATE OF DELIVERY
</div>

<div class="detail-box">
<input type="date">
</div>

<div class="small-label">
ANIMAL NO./SHARE NUMBER
</div>

<div class="detail-box">
<input type="text" value="1/4">
</div>

<div class="donation-box">

<label class="donation-label">

<input type="checkbox" id="donateShare">

Do you want to donate your share?

</label>

</div>

</div>

</div>

<!-- TABLE -->

<table>

<thead>

<tr>
<th>#</th>
<th>Animal No./Share</th>
<th>Name</th>
<th>Price</th>
<th>Total</th>
<th>Remove</th>
</tr>

</thead>

<tbody id="tableBody">

<tr>

<td>1</td>

<td>
<input type="text" class="share-input" value="1/7">
</td>

<td>
<input type="text" class="name-input" placeholder="Enter name">
</td>

<td>4600</td>

<td>4600</td>

<td>
<button class="remove-btn" onclick="removeRow(this)">
×
</button>
</td>

</tr>

</tbody>

</table>

<button class="add-btn" onclick="addRow()">
Add Share
</button>

<div class="total">
Total: ₹ <span id="grandTotal">4600</span>
</div>

</div>

<!-- BUTTONS -->

<div class="bottom-buttons">

    <button class="download-btn" onclick="saveAndDownload()">
        Download PDF
        </button>

<button class="whatsapp-btn" onclick="sendWhatsApp()">
Send WhatsApp
</button>

</div>

<script>

const PRICE = 4600;

const SCRIPT_URL =
"https://script.google.com/macros/s/AKfycbyvatdSzJBcS5An1K4vO7Z3sKlNbAf4F-jt4xUc1HT2LwxkQBXMmv81eQCxhJbxRa8s/exec";
    
    /* ADD ROW */
    
    function addRow(){
    
        const tbody =
        document.getElementById("tableBody");
    
        const rowCount =
        tbody.rows.length + 1;
    
        const row =
        tbody.insertRow();
    
        row.innerHTML = `
    
        <td>${rowCount}</td>
    
        <td>
            <input
            type="text"
            class="share-input"
            value="${rowCount}/7">
        </td>
    
        <td>
            <input
            type="text"
            class="name-input"
            placeholder="Enter name">
        </td>
    
        <td>${PRICE}</td>
    
        <td>${PRICE}</td>
    
        <td>
            <button
            class="remove-btn"
            onclick="removeRow(this)">
            ×
            </button>
        </td>
    
        `;
    
        updateTotal();
    
    }
    
    /* REMOVE */
    
    function removeRow(button){
    
        button.parentElement
        .parentElement
        .remove();
    
        refreshRows();
    
        updateTotal();
    
    }
    
    /* REFRESH */
    
    function refreshRows(){
    
        const rows =
        document.querySelectorAll("#tableBody tr");
    
        rows.forEach((row,index)=>{
    
            row.cells[0].innerHTML =
            index + 1;
    
        });
    
    }
    
    /* TOTAL */
    
    function updateTotal(){
    
        const rows =
        document.querySelectorAll("#tableBody tr");
    
        const total =
        rows.length * PRICE;
    
        document.getElementById(
        "grandTotal"
        ).innerHTML = total;
    
    }
    
    /* WHATSAPP */
    
    function sendWhatsApp(){
    
        const customer =
        document.getElementById(
        "customerName"
        ).value;
    
        let phone =
        document.getElementById(
        "phone"
        ).value;
    
        const address =
        document.getElementById(
        "address"
        ).value;
    
        const total =
        document.getElementById(
        "grandTotal"
        ).innerText;
    
        const donate =
        document.getElementById(
        "donateShare"
        ).checked
        ? "Yes"
        : "No";
    
        /* CLEAN NUMBER */
    
        phone = phone.replace(/\D/g,'');
    
        /* INDIA CODE */
    
        if(phone.length === 10){
            phone = "91" + phone;
        }
    
        let shareData = "";
    
        const rows =
        document.querySelectorAll(
        "#tableBody tr"
        );
    
        rows.forEach((row,index)=>{
    
            const share =
            row.querySelector(
            ".share-input"
            ).value;
    
            const name =
            row.querySelector(
            ".name-input"
            ).value;
    
            shareData +=
    `${index+1}. ${share} - ${name}\n`;
    
        });
    
        const message =
    
    `NAIMI QURBANI CENTRE
    
    Customer: ${customer}
    
    Address: ${address}
    
    Donate Share: ${donate}
    
    Shares:
    ${shareData}
    
    Total: ₹${total}`;
    
        const whatsappURL =
    `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
    
        window.open(
            whatsappURL,
            '_blank'
        );
    
    }

    async function saveAndDownload(){

const customer =
document.getElementById("customerName").value;

const phone =
document.getElementById("phone").value;

const address =
document.getElementById("address").value;

const donate =
document.getElementById("donateShare").checked
? "Yes"
: "No";

const total =
document.getElementById("grandTotal").innerText;

const rows = [];

document
.querySelectorAll("#tableBody tr")
.forEach(row=>{

rows.push({

share:
row.querySelector(".share-input").value,

name:
row.querySelector(".name-input").value,

price: PRICE

});

});

const payload = {

customer: customer,
phone: phone,
address: address,
donate: donate,
total: total,
rows: rows

};

try{

await fetch(SCRIPT_URL,{

method:"POST",

mode:"no-cors",

headers:{
"Content-Type":"text/plain"
},

body: JSON.stringify(payload)

});

alert("Saved to Google Sheet");

window.print();

}

catch(error){

console.log(error);

alert("Upload Failed");



}

}
    
    /* AUTO CURRENT BOOKING DATE */

document.getElementById("bookingDate").value =
new Date().toISOString().split('T')[0];

updateTotal();



    
    </script>

</body>
</html>
