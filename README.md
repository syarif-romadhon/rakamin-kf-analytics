# Kimia Farma Big Data Analytics Project Based Internship Program - June 2024
by Syarif Romadhon

## Project Description
As a Big Data Analytics Intern at Kimia Farma, you'll be tasked with evaluating the company's business performance from 2020 to 2023. This project will require a deep understanding of data and strong analytical skills. Here's a breakdown of the key tasks involved:
1. Importing Dataset to BigQuery
2. Create “tabel analisa”
3. Create Dashboard Performance Analytics Kimia Farma Business Year 2020-2023

### Importing Dataset to BigQuery
Import the four datasets to become a table in BigQuery, the table name is the name of the dataset, but without ".csv"
- kf_final_transaction.csv ([link](https://drive.google.com/file/d/1iDOBdKZ4-kkLhpklQWWrsFvACtI7MCz3/view?usp=sharing))
- kf_inventory.csv ([link](https://drive.google.com/file/d/1ihtG2t0V1AO0IAGkGwQaqtba6AxDEKDI/view?usp=sharing))
- kf_kantor_cabang.csv ([link](https://drive.google.com/file/d/1vzaasqIeXqqe_jI99dNLaa8nxnoe9OWW/view?usp=sharing))
- kf_product.csv ([link](https://drive.google.com/file/d/1739wO7BwtVStHCA4Dcj9xGhlc_blBNbT/view?usp=sharing))

### Create “Tabel Analisa”
Create an analysis table based on the aggregated results of the four imported tables. The following are the mandatory columns in the table:
- transaction_id : kode id transaksi,
- date : tanggal transaksi dilakukan,
- branch_id : kode id cabang Kimia Farma,
- branch_name : nama cabang Kimia Farma,
- kota : kota cabang Kimia Farma,
- provinsi : provinsi cabang Kimia Farma,
- rating_cabang : penilaian konsumen terhadap cabang Kimia Farma
- customer_name : Nama customer yang melakukan transaksi,
- product_id : kode product obat,
- product_name : nama obat,
- actual_price : harga obat,
- discount_percentage : Persentase diskon yang diberikan pada obat,
- persentase_gross_laba : Persentase laba yang seharusnya diterima dari obat dengan ketentuan berikut:
Harga <= Rp 50.000 -> laba 10%
Harga > Rp 50.000 - 100.000 -> laba 15%
Harga > Rp 100.000 - 300.000 -> laba 20%
Harga > Rp 300.000 - 500.000 -> laba 25%
Harga > Rp 500.000 -> laba 30%,
- nett_sales : harga setelah diskon,
- nett_profit : keuntungan yang diperoleh Kimia Farma,
- rating_transaksi : penilaian konsumen terhadap transaksi yang dilakukan.

