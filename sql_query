CREATE TABLE kimia_farma.tabel_analisa AS
WITH product_table AS 
(
  SELECT 
    product_id,
    product_name,
    price,
    CASE 
      WHEN price <= 50000 THEN 0.1
      WHEN price > 50000 AND price <= 100000 THEN 0.15
      WHEN price > 100000 AND price <= 300000 THEN 0.20
      WHEN price > 300000 AND price <= 500000 THEN 0.25
      WHEN price > 500000 THEN 0.3
    END AS persentase_gross_laba
  FROM kimia_farma.kf_product
)
SELECT
  ft.transaction_id,
  ft.date,
  ft.branch_id,
  kc.branch_name,
  kc.kota,
  kc.provinsi,
  kc.rating AS rating_cabang,
  ft.customer_name,
  ft.product_id,
  p.product_name,
  ft.price AS actual_price,
  ft.discount_percentage,
  p.persentase_gross_laba,
  ft.price - (ft.price * ft.discount_percentage) AS nett_sales, # nett_sales = intial_price - discount_price
  (ft.price * p.persentase_gross_laba) - (ft.price * ft.discount_percentage) AS nett_profit, # nett_profit = expected_profit - discount_price
  ft.rating AS rating_transaksi
FROM kimia_farma.kf_final_transaction AS ft
LEFT JOIN kimia_farma.kf_kantor_cabang AS kc
  ON ft.branch_id = kc.branch_id
LEFT JOIN product_table AS p
  ON ft.product_id = p.product_id
;
