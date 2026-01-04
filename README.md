# TasteBuds Catering Service (TBCS)

Quiz 2 Assignment - SWE4302
Student Id: 230042156

## Overview

The problem was solved using a modular structure, following the ooc principles.
This allows on easy extension and maintenance of the codebase, since it follows separation of concerns and uses interfaces and abstract classes to define contracts between different components.
The project can be easily extended, by adding necessary services or models without modifying existing code, since it follows modular structure.
For example, if you want to add Dine-In service, you can create a new service class implementing the necessary interface without changing existing classes.




## Design

The design follows a layered, object-oriented approach. High-level UML:

![UMl](./img/uml.png)

## Demonstration Output


Example output screenshots:

![Output](./img/output2.png)



## Project Structure (recommended organization)
```text
src/
├── core/     // allows relation between multiple modules
│ └── QueueManager.java
│
├── kitchen/
│ ├── KitchenService.java
│ └── HeadChef.java
│
├── customer/
│ ├── OrderService.java
│ ├── DeliveryService.java
│  
│── order/
│ └── Order.java
│ └── OrderService.java
│ 
├── delivery/
│ ├── deliveryService.java
│ └── Delivery.java
│ 
```
This repository follows the same breakdown inside `src/main/java/org/example/` where modules group `Core`, `Customer`, `Kitchen`, `Delivery`, and `Order` responsibilities.


### Running the Project

- Build with Maven:

```bash
mvn clean package
```

- Run the demo/main class (IDE or):

```bash
mvn exec:java -Dexec.mainClass="org.example.Main"
```

Adjust `mainClass` as needed for the project entry.

### Testing

- Unit tests are present under `src/test/java` and can be executed with:

```bash
mvn test
```

tests focused on services and business rules (discount calculations, queueing, delivery assignment logic, and driver checkout validation).

