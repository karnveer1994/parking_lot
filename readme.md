# Parking Lot

## How to Run
The solution source code is in `lib`
 and the unit test for the solution is in `spec` folder.

This solution is using Ruby programming language and RSpec gem for unit testing.

Following are some instructions on how to run the solution:
* 
* cd parking_lot/
* bundle instal
* ruby lib/main.rb
* ruby lib/main.rb inputs.txt > output.txt(in project output file)
    or
* ruby lib/main.rb inputs.txt
* bundle exec rspec


Input:
create_parking_lot 6
park MH-01-HH-1445 White
park TN-01-HB-9999 Yellow
park MH-01-BB-1001 Black
park TN-01-HH-7007 Red
park MH-01-HH-2991 Blue
park KA-01-HH-3991 Silver
leave 4
status
park KA-01-P-333 White
park DL-12-AA-9999 White
registration_numbers_for_cars_with_colour White
slot_numbers_for_cars_with_colour White
slot_number_for_registration_number KA-01-HH-3991
slot_number_for_registration_number MH-04-AY-6666

Output:
Created a parking lot with 6 slots
Allocated slot number: 1
Allocated slot number: 2
Allocated slot number: 3
Allocated slot number: 4
Allocated slot number: 5
Allocated slot number: 6
Slot number 4 is free
Slot No.    Registration No    Colour
1           MH-01-HH-1445      White
2           TN-01-HB-9999      Yellow
3           MH-01-BB-1001      Black
5           MH-01-HH-2991      Blue
6           KA-01-HH-3991      Silver
Allocated slot number: 4
Sorry, parking lot is full
MH-01-HH-1445, KA-01-P-333
1, 4
6

## Class
Following are brief explanations of each class on this solution:
* **Car** : Implemented on `lib\car.rb` to represent Car which is parked on the parking lot. This class store the color and registration number of each car.

* **ParkingLot** : Implemented on `lib\parking_lot.rb` as Parking Lot area on which the Car is parked. This class uses array as the parking slot and implement the logic to park a car on certain slot, to look for cars with certain category (registration number or color) and to remove car from certain parking slot.

* **ParkingSystem** : Implemented on `lib\parking_system.rb`. This class act as interface between the user and the `ParkingLot`. This class uses `Utilities` class as a module to receive user's command and print the requested data to user on proper format. The processed user input is parsed then proper function matched user's query is called.

* **Utilities** : Implemented on `lib\utilities.rb`. This class receives and process user's command so it can be parsed by `ParkingSystem`. This class also used to format and print returned value,
