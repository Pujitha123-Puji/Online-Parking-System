**Title of the Project**: Online Parking System

**PROJECT AIMS AND OBJECTIVES**:
The aims and objectives are as follows:
•To allows employees to view and reserve parking slots for specific dates and times via a mobile app or web application.
•The system helps an individual to pre-book the parking spot from the distant area, reducing traffic congestion and allowing a user to know the availability of parking space in advance.
•The basic objective of a smart parking solution is to identify a vehicle's presence or absence in a particular parking space with a high degree of accuracy, and to pass on this data into a system for visualization and analysis – to be available for parking asset managers and/or enforcement officers.

**Algorithm of the Project**:
Step 1: Start
Step 2: User Registration: Users create an account with their details.
Step 3: Search Availability: Users search for parking spaces based on location, date, and time.
Step 4: Parking Space Selection: Users select a parking space from the available options.
Step 5: Booking Confirmation: Users confirm the booking and receive a confirmation with details.
Step 6: Payment: Users make the payment for the selected parking space.
Step 7: Arrival and Check-in: Users arrive at the parking location and check-in using their booking details.
Step 8: Parking Duration: The system monitors the parking duration based on the user's check- in and check-out times.
Step 9: Check-out and Payment Settlement: Users check out of the parking space and any additional charges are settled.
Step 10: User Feedback: Users have the option to provide feedback on their parking experience.
Step 11: Cancellation and Refunds: Users can cancel their parking booking and request a refund if needed, based on the system's cancellation policy.
Step 12: Booking Modifications: Users have the option to modify their booking details, such as changing the date or time of their parking reservation.
Step 13: Notifications and Reminders: The system sends notifications and reminders to users regarding their upcoming parking reservations.
Step 14: Feedback Analysis and Improvements: The system analyses user feedback to identify areas for improvement and make necessary enhancements to the parking system.
Step 15: Security and Safety Measures: The system ensures the safety and security of parked vehicles through measures like surveillance cameras, secure access points, and emergency protocols.
Step 16: Integration with Navigation Apps: The parking system may integrate with navigation apps to provide users with directions to their selected parking space.

**Code**:
HTML Code:
<! DOCTYPE html>
<html lang=”en”>
<head>
<meta charset=”UTF-8”>
<meta name=”viewport” content=”width=device-width,initial- scale=1.0”>
<link rel=”stylesheet” herf=”styles.css”>
<title>Parking System</title>
</head>
<body>
<h1>Parking System</h1>
<form id=”park form”>
<label for=”licence plate”>Licence Plate:</lable>
<input type=”text” id=”remove Licence Plate” required>
<button type=”button” onclick=”remove Car ()”>RemoveCar</button>
</form>
<button onclick=”view Parked Cars ()”>View Parked Cars</button>
<div id=”result”></div>
<script src=”script.js”></script>
</body>
</html>

**INDE X.CSS**:
Body
{

font-family: Arial, sans-serif; margin: 20px;
}


form, button
{

margin-bottom: 10px;
}

**JAVA PROGRAM**:
let parked Cars = []; function park Car ()
{

const license Plate = document.get Element by Id ('license Plate').value; if (license Plate.trim () === '')
{

alert (‘please enter a license plate.'); return;
}

parked Cars.push (license Plate);
Update Result (“Car parked successfully. Total parked cars :${ parked Cars.length}’); Clear Form ('park Form');
}

function remove Car ()
{
const license Plate to Remove = document. Get Element by Id ('remove LicensePlate')
.value;
const index To Remove = parked Cars. Index Of (license Plate to remove); if (index To Remove! = = -1)
{
Parked Cars. splice (index To Remove, 1);
Update Result (“Car removed successfully. Total parked cars: ${parked Cars.length}”);
}
else
{

Update Result (‘the car is not parked here.');
}

Clear Form ('remove Form');
}

function view Parked Cars ()
{

  if (parked Cars. Length = = = 0)
  {
    Update Result (‘there are no parked cars.');
  }
  Else
  {
  Update Result (`Parked cars: ${parked Cars.join (', ')
  }
}
function update Result (message)
{

Document.get Element by Id ('result').inner Text = message;
}

function clear Form (form Id)
{

document.get Element by Id (form Id).reset ();
}

**JAVA CODE**:
import java.util.ArrayList; import java.util.Scanner; Public class Parking System
{

Static int totalSlots, availableSlots;
Static ArrayList<String> parkedCars = new ArrayList<String> (); Public static void main (String [] args)
{

Scanner sc = new Scanner (System.in);
System.out.println ("Enter the total number of parking slots :"); TotalSlots = sc.nextInt();
AvailableSlots = totalSlots; While (true)
{

System.out.println ("\nWhat would you like to do?"); System.out.println ("1. Park a car"); System.out.println ("2. Remove a car"); System.out.println ("3. View parked cars");
System.out.println ("4. Exit"); int choice = sc.nextInt (); switch (choice)
{


Case 1:
        park Car (); 
        break;
Case 2:
        removeCar ();
        break;
Case 3:
        viewParkedCars ();
        break;
Case 4:
        System. Exit (0);
default:
        System.out.println ("Invalid choice. Please try again.");
}
}
}

Public static void park Car ()
{

if (availableSlots == 0)
{

System.out.println ("Sorry, there are no available parking slots.");
return;
}

Scanner sc = new Scanner(System.in);
System.out.println ("Enter the license plate number of the car :"); String licensePlate = sc.nextLine(); parkedCars.add(licensePlate);
availableSlots--;
System.out.println ("Car parked successfully. Available slots: " + availableSlots);
}

public static void removeCar()
{

if (availableSlots == totalSlots)
{

System.out.println("There are no parked cars."); return;
}

Scanner sc = new Scanner(System.in);
System.out.println("Enter the license plate number of the car to be removed:");
String licensePlate = sc.nextLine();
if (parkedCars.contains(licensePlate))
{

parkedCars.remove(licensePlate); availableSlots++;
System.out.println("Car removed successfully. Available slots: " +	availableSlots);
}
else
{

System.out.println("The car is not parked here.");
}
}

public static void viewParkedCars()
{

if (availableSlots == totalSlots)
{

System.out.println("There are no parked cars.");

return;
}

System.out.println("Parked cars:"); for (String licensePlate : parkedCars)
{

System.out.println(licensePlate);
}
}
}

OUT PUT :
Enter the total number of parking slots: 123
What would you like to do?
1.Park a car
2.Remove a car
3.View parked cars
4.Exit 1
Enter the license plate number of the car: 23
Car parked successfully. Available slots:
122
What would you like to do?
1.Park a car
2.Remove a car
3.View parked cars
Exit 






