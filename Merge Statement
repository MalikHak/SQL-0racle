
-- MAKE SURE YOU FIRST RUN THE merge_sql_example FILE AS SHOWN IN THE VIDEO 


MERGE INTO existing_customers c
USING new_customers n
ON (c.customer_id = n.customer_id)
WHEN MATCHED THEN
    UPDATE SET
    c.first_name = n.first_name,
    c.last_name = n.last_name,
    c.address_state = n.address_state,
    c.email_address = n.email_address
WHEN NOT MATCHED THEN
    INSERT (c.customer_id, c.first_name, c.last_name, c.address_state, c.email_address)
    VALUES (n.customer_id, n.first_name, n.last_name, n.address_state, n.email_address)


SELECT * FROM existing_customers


MERGE INTO existing_customers c
USING new_customers n
ON (c.customer_id = n.customer_id)
WHEN MATCHED THEN
    UPDATE SET
    c.first_name = n.first_name,
    c.last_name = n.last_name,
    c.address_state = n.address_state,
    c.email_address = n.email_address
DELETE WHERE c.first_name = 'John'
WHEN NOT MATCHED THEN
    INSERT (c.customer_id, c.first_name, c.last_name, c.address_state, c.email_address)
    VALUES (n.customer_id, n.first_name, n.last_name, n.address_state, n.email_address)


