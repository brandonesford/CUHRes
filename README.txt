Description:
	 This is our submission for 3004 D4.


	Installation Instructions:
    Run the shell script using:
	chmod +x start.sh
	./start.sh

	OR

	source ./start.sh

	(if for what ever reason the shell script does not run, it is composed of the following lines
	   qmake
	   make
	   ./CodeRedCOMP3004
	)


	Application Interaction Instructions:
	The program starts with a prompt to login. Using the number '1' allows access as a payroll specialist.
	After the login comes a page with a summary of the employees.
	The filter works for last name only.
	The apply raises brings you to a seperate page on which you can apply a raise to either staff or faculty.
	Clicking on the name of an employee in the list brings you to the edit page of that employee. 
	On the edit page there is information regarding everything from their name, wage, role, etc. 
	Information can be edited and saved on this page.
	The save is then transfered over to the database. 
	You can cancel back to the main page, or log out.
	There are help boxes to provide some help with how to operate the system.


	Data Integration Tool Description:
	The data integration tool operates on transaction files (ie 'transaction.cunics').
	The file is parsed and the information is updated to the database.

	An added benefit of the way our transaction file is designed is that it is human readable.
	You should be able to see what is being changed just by looking at the file.

	Cheers :)


	Data Integration Tool Instructions:
	1) Navigate to Data Integration Tool page
	2) Select the "Import File", and choose a transaction file
	NOTE: The transaction files are stored in the project directory under:
	  'transactions/transaction.cunics' - File containing modification transactions (USE THIS)
	  'transactions/init.cunics' 	    - File containing employees to init DB
					      (This is executed by our system automatically at run time.
					      You DO NOT need to run this)
	3) Select "Update" to execute the transaction file
	  You will be prompted on a success/fail state
	4) Select "Back" to navigate back to the Employee summary page

	The specific actions being done by the 'transaction.cunics' transaction file are as followed:
	- Raise being applied to staff
	- Updating employee with ID '12'
	- Updating employee with ID '5'
	- DestroyRole for ID '1' (TA)
	- Raise being applied to faculty
	- Adding employee (Tony Stark)
	- Updating employee with ID '30'
	- Updating employee with ID '46'
	- Updating employee with ID '44'
	- Updating employee with ID '25'
	- Adding employee (Billy Bones)
	- Updating employee with ID '47'

Program Authors:
	Menna Ahmed
	Scott Ellerington
	Brandon Esford
	Bernard Laveaux

Sources:
	CodeRedCOMP3004.pro
	start.sh
	applyraisescontrol.cpp
	cuhresdataprocessor.cpp
	cuhresparser.cpp
	cunicsdb.cpp
	employee.cpp
	employeecontrol.cpp
	employeeorm.cpp
	employeeposition.cpp
	main.cpp
	mainwindow.cpp
	netpay.cpp
	payrollspecialist.cpp
	payrollspecialistorm.cpp
	paystub.cpp
	role.cpp
	roleorm.cpp
	user.cpp
	username.cpp
	userorm.cpp
	workterm.cpp
Headers:
	applyraisescontrol.h
	cuhresdataprocessor.h
	cuhresparser.h
	cunicsdb.h
	employee.h
	employeecontrol.h
	employeeorm.h
	employeeposition.h
	main.h
	mainwindow.h
	netpay.h
	payrollspecialist.h
	payrollspecialistorm.h
	paystub.h
	role.h
	roleorm.h
	user.h
	username.h
	userorm.h
	workterm.h
Transaction Files:
	transactions/transaction.cunics
	transactions/init.cunics
	
