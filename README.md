
# AmazonProductSales-Dashboard

## DataSet
<a href=https://github.com/ABHI91827/AmazonProductSalesDasboard/blob/main/amazon_products_sales_data_cleaned.xlsx>Amazon Dateset</a>






### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present .
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for four fields names ProductCategory,Sponsored,Delivery_date and Data Collected date.
## Business problems 
-Total sales by product ProductCategory.

-Average discount percentage.

-reviwes by ProductCategory.

-Total revenue by ProductCategory.

-revenue by Sponsored.

-revenue uplift by discount.
## DAX
-Total revenue:

        =sum(Product_sale_lastmonth).

-Total OriginalPrice:

        =sum(OriginalPrice).

-Average discount:

        =Average(discount_price).
-Totalsales:

        =count(Product_sale_lastmonth).
-Actual_revenue:  

        =sumx('amazonProductSale',discounted_price-Product_sale_lastmonth).

-Baseline Actual_revenue:

      =sumx('amazonProductSale',original_price-Product_sale_lastmonth).
## DASHBOARD


-Revenue uplift:

        =sumx('amazonProductSale',original_price-discounted_price *Product_sale_lastmonth).
## DASHBOARD
<a href =https://github.com/ABHI91827/AmazonProductSalesDasboard/blob/main/Amazon_sales_dashboard.pbix>view Dashboard</a>
       

