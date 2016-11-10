Car Dealer Inventory System
Let us consider that we will develop Car Dealer Inventory System (referred as System). The System would have the ability to manage vehicles in the inventory. As well as generate report on the current inventory state. Here are some of the entities involved in the System.
 
Vehicle has following properties.
 
- id
- type - This property have the following set of values
	- Truck
	- Sedan
	- Van
- color
- make - This property have the following set of values
	- DODGE, FORD, HONDA, HYUNDAI, CHEVROLET
- year
- towingCapacity - only truck requires this property
- passengerCapacity - only van requires this property

- msrp - The System gets the manufacturer’s suggested retail price from a third part library. MSRPProvider. This implements the following interface
```java
public interface  MSRPProvider {
	public double getMSRPForLargeVehicle(String make, int year); // For Trucks or Van
	public double getMSRPForSmallVehicle(String make, int year); // For Sedan or hatch back
}
```
 
Inventory should have a data structure to hold the all the vehicles available to the dealer. It should provide the functionality to perform the basic CRUD operations.
 
Report should allow to retrieving Vehicle information from the Inventory by Type, Year, and Make.