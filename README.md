# Car Dealer Inventory System
We will develop a Car Dealer Inventory System (referred to as the System). The System would have the ability to manage vehicles in the inventory, as well as generate a report on the current inventory state. 

Here are some of the entities involved in the System.
 
Vehicle has the following properties.
 
- id
- type - This property has the following set of values
	- Truck
	- Sedan
	- Van
- color
- make - This property has the following set of values
	- DODGE, FORD, HONDA, HYUNDAI, CHEVROLET
- year
- towingCapacity - only truck requires this property
- passengerCapacity - only van requires this property
- msrp - The System gets the manufacturer’s suggested retail price from a third party library, MSRPProvider, which implements the following interface
```java
public interface  MSRPProvider {
	public double getMSRPForLargeVehicle(String make, int year); // For Trucks or Van
	public double getMSRPForSmallVehicle(String make, int year); // For Sedan
}
```
 
Inventory should have a data structure to hold all of the vehicles available to the dealer. It should provide the functionality to perform the basic CRUD operations.
 
Report should allow retrieval of Vehicle information from the Inventory by Type, Year, and Make.