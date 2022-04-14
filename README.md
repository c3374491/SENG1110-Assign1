*Can't remember the result for this assignment, however, I did receive a HD for this course.*
# SENG1110-Assign1
Assignment 1: Vet Clinic Management [Java] 
<nl>
<nl>
## INCLUDED FILES
 - Clinic.java
 - Doctor.java
 - Pet.java

## INTRODUCTION
The objective of this assignment is to implement an object-oriented program using Java, to manage doctors and pets in
a vet clinic. Assignment 2 will be an extension of this assignment.

## SPECIFICATION
The program will keep track of up to 2 doctors, and up to 4 pets.
When run, the program will display a menu of actions to the user, including one that exits the program. Until the user
chooses to exit, the menu is displayed again after each action is completed.

The program must have the following functionalities:

 1. The user may enter a new doctor into the vet clinic. The user will input the name and specialisation. If a doctor with the same name already exists, or the specialisation is invalid, or the doctor limit has been reached, the program should output an error message.
2. The user may enter a new pet into the vet clinic. The user will input the name, type, size, weight, and age. If a pet with the same name already exists, or an invalid value is given, or the pet limit has been reached, the program should output an error message.
3. The user may delete a doctor from the vet clinic. The user will input the name of the doctor. If the doctor does not exist, the program should output an error message. Before deletion, all pets that are assigned to the specified doctor should have their 'doctor' instance variable updated to "No doctor assigned".
4. The user may delete a pet from the vet clinic. The user will input the name of the pet. If the pet does not exist, the program should output an error message.
5. The user may request a list of doctors in the vet clinic with all the information of each doctor. Normally, one line should be output for each doctor, with the form: Doctor *NAME*: *SPECIALISATION* specialist. If there are no doctors, the program should output the message "No doctors".
6. The user may request a list of pets in the vet clinic with all the information of each pet. Normally, one line should be output for each pet, with the form: "Pet *NAME*: *SIZE* *TYPE* weighing *WEIGHT* kg at *AGE* years old (*DOCTOR*)." If there are no pets, the program should output the message "No pets".
7. The user may request a list of pets assigned to a specific doctor. The user will input the name of the doctor. Normally, one line should be output for each pet, similarly to above. If there are no doctors, the program should
output "No doctors". If the named doctor does not exist, the program should output "No doctor with that name". Otherwise, if the doctor has no assigned pets, the program should output "No assigned pets".
8. The user may assign a doctor to a pet. The user will input the name of the pet and the name of the doctor. If the pet or doctor do not exist, or the pet is already assigned to that doctor, or the doctor does not have the right
specialisation, the program will output an error message. If the pet is already assigned to another doctor, the program should ask the user to confirm that they would like to change the assigned doctor.
9. The user may analyse a pet. The user will input the name of the pet and the program will output an indication of whether the pet is overweight.
##### A cat is considered overweight if it is:
	- Small with weight greater than 4kg
	- Medium with weight greater than 6kg
	- Large with weight greater than 8kg
##### A dog is considered overweight if it is: 
	- Small with weight greater than 6kg
	- Medium with weight greater than 9kg
	- Large with weight greater than 12kg
If the pet does not exist, the program will output an error message.

*Doctor and pet names should be converted to lowercase after input. For example, if the user inputs "Benny", the
program should convert it to "benny".*

## PROGRAM REQUIREMENTS

Your program should consist of three classes, with these names and instance variables:

 - Doctor – stores the following details about a doctor.
	 - name – String – the name of the doctor. Should not contain spaces.
	- specialisation – String – the specialisation of the doctor. Must be "dog" or "cat".
- Pet – stores the following details about a pet.
	- name – String – the name of the pet. Should not contain spaces.
	- type – String – the type of the pet. Must be "cat" or "dog".
	- size – String – the size of the pet. Must be "small", "medium" or "large".
	- weight – double – the weight of the pet. Must be positive.
	- age – int – the age of the pet. Must be positive.
	- doctor – String – the doctor of the pet. Should initially be "no doctor assigned".
- Clinic – provides information for all doctors and pets in the clinic.
	- doctor1, doctor2 – Doctor – up to two doctors.
	- pet1, pet2, pet3, pet4 – Pet – up to four pets.

All instance variables of your classes need to be **private** (this is imposed so that you apply the principles of **encapsulation**).
Your classes will need methods to provide the required functionalities. The only class which should have a **main method** is Clinic.java, which should create an instance of the class Clinic, and call a method run(), which will display the menu to the user. This class will be the only one that takes input from and sends output to the user. It may do so using either TIO or GUI methods (your choice). A template is shown below.

```java
public class Clinic {
	private void run(){
		//...
	}
	public static void main(String[] args){
		Clinic c = new Clinic();
		c.run();
	}
}
```

You **must not use arrays** in this assignment.
**Marks** will be awarded for layout (including visual aspects (variable names, indentation) and structural aspects (variable scope, method usage)), documentation (comments), and the submission's ability to perform as specified.
