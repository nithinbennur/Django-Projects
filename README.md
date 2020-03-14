# Django-projects
1)Creating the Project Using the Command
		C:\djangoproject>django-admin startproject form_project

	2)Inside the Project, we have to create the Applications
       		a)	C:\djangoproject>cd form_project

       		b)	C:\djangoproject\form_project>python manage.py startapp firstapp

			C:\djangoproject\form_project>

	3)Commands to create the table by referencing to model class,we have to use the following command
			a)	python manage.py makemigrations

				C:\djangoproject\form_project
				C:\djangoproject\form_project\template
				C:\djangoproject\form_project\static
				Migrations for 'firstapp':
  				firstapp\migrations\0001_initial.py
    				- Create model Formdetails
	
			b)	In order to see the table information created using Django Framework,we have to use the command
		
				python manage.py sqlmigrate firstapp 0001
				C:\djangoproject\form_project
				C:\djangoproject\form_project\template
				C:\djangoproject\form_project\static
				--
				-- Create model Formdetails
				--
					CREATE TABLE `firstapp_formdetails` (`id` integer AUTO_INCREMENT NOT NULL PRIMARY KEY, `fullname` varchar(30) NOT NULL, `phone` integer NOT 			NULL, `client_value` integer NOT NULL, `email` varchar(50) NOT NULL, `website` varchar(50) NOT NULL);
	
			c)	In order to execute the prepared query we have to use the following command

				python manage.py migrate
				By default, Django framework would create a column, i.e "id"(A.I) as well as it will be treated as "P.K(primary key)"

	4)Command to run the server
		python manage.py runserver
