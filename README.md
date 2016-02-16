Project: Linux Server Configuration -- [Hyomin Choi] 
====================================

IP address and SSH port
-----------------------
52.35.124.212  -p 2200  
Please type the following :  
ssh -i ~/.ssh/udacity_key.rsa grader@52.35.124.212 -p 2200  


Complete URL to Catalog Web App hosted by the server  
-----------------------------------------------------
http://ec2-52-35-124-212.us-west-2.compute.amazonaws.com/  


Summary of Catalog Web App and Configuration changes 
-----------------------------------------------------
* Vertual environment was set up for the python Flask Frameworks
* Database is setup using PostgreSQL:
	* the database 'catsupplies' is created by user 'grader'  
	* 3 tables in the db: category, supply_items, user
	* a user 'catalog' has limited permission to db 'catsupplies' (select,insert on tables)
* Appropriate changes had to made for the following files:  
	* Apache configuration file /etc/apache2/sites-enabled/000-default.conf
	* app.wsgi file is in /var/www/catalog  
	* the source files of catalog app are lcoated in /var/www/catalog/catalog
	* the main python file is named __init__.py
	* redirect and javascript origin addresses were added to client_secrets.json 


Useful Information/Resources
-----------------------------
* PSQL granting/revoking privileges to another user:  
http://www.postgresql.org/docs/8.3/static/sql-grant.html  
http://www.postgresql.org/docs/9.1/static/sql-revoke.html  


