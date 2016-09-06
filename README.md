
#CREATE A NEW DATABASE 
@ terminal
sqlite3 cats_database.db

@ sqlite
.quit

#CREATE A CAT TABLE AND MODIFY A COLUMN 
@ terminal  
sqlite3 cats_database.db < 01_create_cats_table.sql  
sqlite3 cats_database.db < 02_add_column_to_cats.sql  
sqlite3 cats_database.db  

@ sqlite  
.schema 
.quit

#INSERT CATS INTO CAT TABLE 
@ terminal  
sqlite3 cats_database.db < 03_insert_cats_into_cats_table.sql  
sqlite3 cats_database.db

@ sqlite  
SELECT * FROM cats
.quit

#UPDATE A CAT'S NAME
@ terminal   
sqlite3 cats_database.db < 04_update_cats_name.sql     
sqlite3 cats_database.db  

@ sqlite    
SELECT * FROM cats  
.quit 

#REMOVE A "CAT" FROM CAT TABLE  
@ terminal  
sqlite3 cats_database.db < 05_update_cats_name.sql  
sqlite3 cats_database.db  

@ sqlite  
SELECT * FROM cats  
.quit  




