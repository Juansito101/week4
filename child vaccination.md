Child vaccination chart







Action
1. Insert Function

Create a function insert() that takes the following inputs:
Patient’s first name
Patient’s last name
The birth month when the vaccine was administered (as an integer)
Refer to the sample sheetLinks to an external site. for guidance.
Use a loop where appropriate.





deg insert():
	first_name = input("first name: ")
	last_namen = input("last name: ")

  # Loop for valid month is entered
    while True:
        try:
	 birth_month = int(input("Birth month (1-12) when vaccine was administered: "))
            if 1 <= birth_month <= 12:
                break
            else:
                print("Please enter a valid month between 1 and 12.")
        except ValueError:
            print("Invalid input. Please enter an integer between 1 and 12.")

 # Store patient info as a dictionary
    patient_record = {
        "first_name": first_name,
        "last_name": last_name,
        "birth_month": birth_month
    }

    # Append to the patients list
    patients.append(patient_record)
    print("Patient record added successfully!")



#create list where its records data
patients = []

def insert():
    first_name = input("first name: ")
    last_name = input("last name: ")
    
    # Loop until a valid month is entered
    while True:
        try:
            birth_month = int(input("birth month (1-12) when vaccine was administered: "))
            if 1 <= birth_month <= 12:
                break
            else:
                print("Please enter a valid month between 1 and 12.")
        except ValueError:
            print("Invalid input. Please enter an integer between 1 and 12.")

    # Record patient info as a dictionary
    patient_record = {
        "first_name": first_name,
        "last_name": last_name,
        "birth_month": birth_month
    }

    # Add to the patients list
    patients.append(patient_record)
    print("Patient record added successfully!")








2. Data Structure

Use a nested dictionary to store patient data.

The main dictionary should be named patient.

Each patient record should be stored under a unique record number (serving as the key).

Each record number corresponds to one patient and contains a nested dictionary of key–value pairs for that patient’s details.





# dictionary to store patients records
patient = {}

record_number = 1

def insert():
    global record_number  # Use counter

    first_name = input("Enter first name: ")
    last_name = input("Enter last name: ")

    # Loop until a valid birth month is entered
    while True:
        try:
            birth_month = int(input("Enter the birth month (1-12) when vaccine was administered: "))
            if 1 <= birth_month <= 12:
                break
            else:
                print("Please enter a valid month between 1 and 12.")
        except ValueError:
            print("Invalid input. Please enter an integer between 1 and 12.")

    # Nested dictionary for records
    patient_record = {
        "first_name": first_name,
        "last_name": last_name,
        "birth_month": birth_month
    }

    # Insert into the main patient dictionary 
    patient[record_number] = patient_record
    print(f"Patient record added successfully under record number {record_number}!")



















3. Verification

Ensure that the patient dictionary contains all the entered data.

Call the insert() function again to add another patient record.
The new record should be appended without overwriting existing data.
Verify that the dictionary now contains both records.







  

4. Code Requirements

Clearly demonstrate the working of all the tasks mentioned above.
Include comments in the code for readability.
Write the Python code in Markdown format (for GitHub submission).
Record a video explanation of your code and its output.
Use of AI tools
If there is any suspicion of AI-generated work, the student will be required to complete a new graded activity in person. This replacement activity will determine the final grade for that assignment.

Rubric
Each response is worth 2.5 points. You must provide a detailed explanation of your code. Failure to upload the video or to adequately explain the code will result in a grade of 0.
