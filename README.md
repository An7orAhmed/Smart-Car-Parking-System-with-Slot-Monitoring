```markdown
# Smart Car Parking System with Slot Monitoring

## Project Description
An automated parking management system that monitors vehicle entry/exit using sensors, controls gate access via servo/motor, and provides real-time slot availability status on an LCD. Supports PIC and Arduino platforms with code written in Proton Basic/C++.

## Key Features
- 6 parking slot sensors with occupied/vacant detection
- Automatic gate opening on vehicle detection
- Visual slot status display via 16x2 LCD
- Gate auto-closing timer with countdown display
- Slot full detection and error handling
- Support for servo motor (Arduino) or DC motor (PIC)

## Pin Configuration

### Proton Basic (PIC 16C72A)
| Component | Pin    | Function   |
|-----------|--------|------------|
| Motor     | PORTC.0| Gate motor |
| Gate      | PORTC.1| Entry gate |
| Slot 1    | PORTC.2| Sensor 1   |
| Slot 2    | PORTC.3| Sensor 2   |
| Slot 3    | PORTC.4| Sensor 3   |
| Slot 4    | PORTC.5| Sensor 4   |
| Slot 5    | PORTC.6| Sensor 5   |
| Slot 6    | PORTC.7| Sensor 6   |

### Arduino (Uno/Nano)
| Component | Pin  | Function       |
|-----------|------|----------------|
| Servo     | D10  | Gate control   |
| Gate      | D3   | Entry sensor   |
| Slot 1    | D4   | Sensor 1       |
| Slot 2    | D5   | Sensor 2       |
| Slot 3    | D6   | Sensor 3       |
| Slot 4    | D7   | Sensor 4       |
| Slot 5    | D8   | Sensor 5       |
| Slot 6    | D9   | Sensor 6       |
| LCD RS    | A0   | LCD Control    |
| LCD E     | A1   | LCD Control    |
| LCD D4-7  | A2-5 | LCD Data Bus   |

## Note on Diagrams
Circuit diagrams and pin configurations may require adjustments based on specific hardware implementations. Always verify connections against your physical components.

## Source Code Structure
- `carParking.bas`: Proton Basic code for PIC microcontroller implementation
- `car_parking.ino`: Arduino code with servo control and LCD interface
- Custom LCD character patterns for vehicle status display
- Motor control routines for two types of actuator mechanisms
```