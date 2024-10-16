# PDM

# Tables:

### 1. Users

- user_id (Primary Key)
- name
- email
- address
- date_of_birth
- phone_number

### 2. Income_Details

- income_id (Primary Key)
- user_id (Foreign Key)
- income_type (e.g., salary, interest, rental)
- amount
- income_date
- source

### 3. Tax_Rules

- rule_id (Primary Key)
- income_type
- tax_rate
- deduction
- effective_date
- expiration_date

### 4. Tax_Calculations

- calc_id (Primary Key)
- user_id (Foreign Key)
- total_income
- total_tax
- calc_date
- tax_year
- status (e.g., pending, completed)

### 5. Deductions

- deduction_id (Primary Key)
- user_id (Foreign Key)
- deduction_type
- amount
- deduction_date

### 6. Payments

- payment_id (Primary Key)
- user_id (Foreign Key)
- calc_id (Foreign Key)
- payment_amount
- payment_date
- payment_method (e.g., bank transfer, credit card)

### 7. Audit_Logs

- audit_id (Primary Key)
- user_id (Foreign Key)
- action (e.g., create, update, delete)
- action_date
- details

### Relationships
Users to Income_Details is a one-to-many relationship.
Users to Tax_Calculations is a one-to-many relationship.
Users to Deductions is a one-to-many relationship.
Users to Payments is a one-to-many relationship.
Users to Audit_Logs is a one-to-many relationship.
Tax_Calculations to Payments is a one-to-many relationship.
Tax_Rules provides lookup data for calculating taxes.




![drawSQL-image-export-2024-10-16](https://github.com/user-attachments/assets/90ca95f9-9801-4038-b792-12c53da2cff0)




note:
https://drawsql.app/teams/tran-hoang-doanh/diagrams/tcs/embed
