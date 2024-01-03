# The Task

You are going to create multiple classes from scratch that meets the guidelines set out below. There are blank files named for each class that are ready for you to work in.

---

## Smartphone

The Smartphone class in `Smartphone.java` is going to mimic the functionality of a smartphone. Here is what it needs to include:

Variables:
- `phoneManufacturer` as a `String` (this would be `"Apple"`, `"Samsung"`, etc.)
- `phoneModel` as a `String` (this would be `"iPhone 15 Pro"`, `"Galaxy S23 Ultra"`, etc.)
- `phoneNumber` as a `String` (this would be like `"###-###-####`)
- `currentBatteryPercent` as an `int` (this would be like 40% is `40`)
- `availableDataGB` as a `double` (this would be like 3.5 GB is `3.5`)
- `hasCase` as a `boolean` (this would be `true` if the phone has a case and `false` if it does not)

Constructors (have a constructor for each listed combination of inputs):
- All variables
- `phoneManufacturer`, `phoneModel`
- `phoneManufacturer`, `phoneModel`, `phoneNumber`
- `phoneManufacturer`, `phoneModel`, `currentBatteryPercent`, `hasCase`

Methods:
- Accessor methods for all variables.
- Mutator methods for `phoneNumber`, `currentBatteryPercent`, `availableDataGB` and `hasCase`. Make sure that `currentBatteryPercent` must be between 0 and 100, inclusive. Make sure that `availableDataGB` cannot be negative.
- `text` prints out a statement. Takes in two `String` parameters as a phone number to text and the message to send. If the provided phone number is the same as the phone's number, print `"Error: Cannot Text Self"`. Otherwise, print `"Sent "Message Here" to ###-###-####"` where `"Message Here"` the message to send and the phone number is filled in.
- `breakFromFall` returns a `boolean` value. Takes in a `double` parameter as a height in feet. If the height is greater than `4.0` and the phone does not have a case, then it breaks and return `true`. If the phone has a case and the height is greater than `6.0`, then it breaks and returns `true`. In all other cases, the phone does not break and return `false`.
- `videosCanWatch` returns an `int` value. Takes in no parameters. Each video consumes `0.2` GB of cellular data to watch. Based on `availableDataGB`, return the number of videos that the available data can still support. i.e. if I have `1.5` GB of data, I can watch `7` `0.2` GB videos before I run out of data.
- `gamePlayTime` returns a `double` value. Each percent of battery can lead to `4` minutes of playtime. Based on `currentBatteryPercent`, return the number of hours of games you can play. i.e. if I have `40` percent battery, then I can play `160` minutes of games, which would return `2.666666666667` hours.
- `toString` that returns a `String` that uses `phoneManufacturer`, `phoneModel`, and `hasCase`. i.e. `"Apple iPhone 15 Pro has a case."` or `"Samsung Galaxy S23 Ultra does not have a case."`
- `equals` method that returns a `boolean` value. Should take in a `Smartphone` as a parameter, and results are based on `phoneManufacturer` and `phoneModel` being the same. If both `phoneManufacturer` and `phoneModel` are equal between the two phones, then return `true`. Otherwise, return `false` as the phones are not equal.

In the `SmartphoneTest.java` file, create at least 4 sample phones (one for each of the constructors, using fake phone numbers when needed). Using combinations of these phones, thoroughly test all methods in the class. This might mean calling a method multiple times with different inputs or with different phones to make sure they work properly.

---

## Elevator

The Elevator class in `Elevator.java` is going to mimic the functionality of an elevator. Here is what it needs to include:

Variables:
- Class variable `manufacturer` as a `String` with the value `"Otis"`
- `currentFloor` as an `int`
- `maxFloor` as an `int`
- `numRiders` as an `int`
- `maxRiders` as an `int`

Constructors (have a constructor for each listed combination of inputs):
- All variables
- `maxFloor`, `maxRiders`

Methods:
- Accessor methods for all variables (including class variable).
- Mutator methods for `currentFloor` and `numRiders`. Ensure that `currentFloor` is not set to a negative or a value above `maxFloor`. Ensure that `numRiders` is not set to a negative or a value above `maxRiders`.
- `callToFloor` will move the elevator's `currentFloor` to a provided `int` parameter value. It will not return anything, but subsequent calls to `currentFloor` accessor method should show that it successfully changed to the requested floor. Cannot move the elevator to a negative floor or to a floor higher than the `maxFloor`.
- `getOnElevator` will increase the elevator's `numRiders` by a provided `int` parameter value. It will not return anything, but subsequent calls to `numRiders` accessor method should show that it successfully increased the number of riders. Should print that it cannot accept more riders if the number of riders to be added would put the elevator over its capacity provided by `maxRiders` and leave `numRiders` unchanged in that situation.
- `getOffElevator` will decrease the elevator's `numRiders` by a provided `int` parameter value. It will not return anything, but subsequent calls to `numRiders` accessor method should show that it successfully decreased the number of riders. Should print that it does not have enough riders if the number of riders to be exited would put the elevator under `0` riders and leave `numRiders` unchanged in that situation.
- `toString` that returns a `String` that uses `manufacturer`, `currentFloor`, `maxFloor`, `numRiders`, and `maxRiders`. i.e. `"This Otis elevator is on floor 1 of 15 with 4 of 15 riders"` or `"This Otis elevator is on floor 6 of 6 with 10 of 10 riders."`
- `equals` method that returns a `boolean` value. Should take in an `Elevator` as a parameter, and results are based on `maxFloor` and `maxRiders` being the same. If both `maxFloor` and `maxRiders` are the same between the two elevators, then return `true`. Otherwise, return `false` as the elevators are not equal.

In the `ElevatorTest.java` file, create at least 3 sample elevators (at least one for each of the constructors). Using combinations of these elevators, thoroughly test all methods in the class. This might mean calling a method multiple times with different inputs or with different elevators to make sure they work properly.

---

## Make Your Own Class

Pick any object that has significance to you (and we haven't already made as a class). Make a new Java file with the name of your class and create it from scratch! Include whatever variables, constructors, and methods you feel it needs. The requirements (minimums):
- 4 variables (at least 3 types)
- 3 constructors
- Relevant accessor and mutator methods
- 3 other methods
- `toString` and `equals` methods
- Comments throughout describing purposes and reasoning for what you made

Use the `MakeYourOwnTest.java` file to create at least 4 sample objects from your class (using each constructor at least once). Using them, thoroughly test all methods in the class.  This might mean calling a method multiple times with different inputs or with different objects to make sure they work properly.