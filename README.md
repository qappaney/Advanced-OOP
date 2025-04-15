# Employee Management System

## Overview
A Python OOP implementation of an employee management system with:
- Person/Employee hierarchy
- Car simulation
- Office management

## Core Classes

### Person (Base Class)
- Tracks: `name, money, mood, healthRate`
- Methods: `sleep(), eat(), buy()`

### Employee (Inherits Person)
- Adds: `id, car, email, salary, distanceToWork`
- Methods: `work(), drive(), refuel()`

### Car
- Manages: `fuelRate (0-100), velocity (0-200)`
- Methods: `run(), stop()`
- Uses property decorators for validation

### Office
- Manages employee roster
- Methods: `hire(), fire(), reward(), deduct()`
- Static: `calculate_lateness()`
- Class: `change_emps_num()`

## Example Usage
```python
samy_car = Car("Fiat 128", 80, 60)
samy = Employee("Samy", 5000, "neutral", "100%", 1, samy_car, "samy@example.com", 10000, 30)

iti = Office("ITI")
iti.hire(samy)

samy.work(8)  # Sets mood to "happy"
samy.drive(30)  # Consumes fuel
iti.check_lateness(1, 8)  # Rewards if on time
