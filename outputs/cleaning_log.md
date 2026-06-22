# Cleaning Log

## 1. List of issues found - 

1. Missing values found in 3 columns - Region , ship_mode & Discount.
2. Duplicate records with exact same information found.
3. For a few order_ids certain records with conflicting information found.
4. Data type and formatting issues like extra spaces identified in columns such as order_date, ship_date, customer_name, segment, category. 
5. Calculation errors found in sales, profit columns.
6. Datatype and invalid values found in discount column.


## 2. Cleaning actions performed

1. Missing values in Region and ship_mode replaced with "Unknown"
2. Exact duplicate records (Count = 20) removed using remove duplicates.
3. Used TRIM function to remove extra/trailing/leading spaces from customer_name, segment, category, ship_mode.
4. standardized order_date & ship_date into yyyy-mm-dd format by using text to columns--> date and then formatting to date type from upper ribbon.
5. Discount : Standardized the discount into a readable % format. Negative and unually high discounts were flagged as invalid. Missing discounts were treated as 0%, if the sales data was matching, else flagged as invalid.
6. Removed exact duplicate records; flagged duplicate order IDs with conflicting information as "Warning".


## 3. Business rules applied

1. Did not include non-completed/failed/refunded records in completed-sales summaries.
2. Flagged negative discounts and unusually high discounts as invalid.
3. Did not include non-completed/failed/refunded records in completed-sales summaries.
4. Removed exact duplicate records; flagged duplicate order IDs with conflicting information as "Warning".

## 4. Assumptions Made 

1. Considered discounts >25% as unusually high and flagged them as invalid.
2. For complete orders summary - Only considered records which were flagged as clean.

## 5. Records removed

20 dulpicate records removed.

## 6. Records flagged 

155 records flagged as invalid or Warned for conflicting information.

## 7. Limitations of your cleaning process

Checked only the columns mentioned in the assignment for data discrepancy / formatting issues. Applied the limited business rules provided. Beyond the above, there is a possibility of data issues in other columns.

