# Mars Rover Mission Control

## 1. Functional Requirements

Functional Requirements describe what the system shall do.

### FR-01: Command Reception
The rover shall receive commands from Mission Control and execute valid commands.

### FR-02: Rover Status Reporting
The rover shall report its current position, battery level, temperature, and communication status.

### FR-03: Command Validation
The system shall reject invalid or unauthorized commands.

### FR-04: Safe Mode
The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

### FR-05: Command Execution Status
Mission Control shall receive command execution status.

### FR-06: Event Recording
All commands and critical rover events shall be recorded with timestamp and operator ID.

### FR-07: Communication Failure Detection
The system shall detect communication failures.

### FR-08: Communication Interruption Handling
The system shall continue operating despite temporary communication interruptions.


## 2. Non-Functional Requirements

Non-Functional Requirements describe the quality and constraints of the system.

### NFR-01: Performance
Command processing should normally complete within 5 seconds after a command is received by the rover.

### NFR-02: Authentication
Only authenticated Mission Control operators shall be permitted to issue rover commands.

### NFR-03: Communication Reliability
The system shall continue operating despite temporary communication interruptions.

### NFR-04: Multiple Rover Support
The system should support communication with multiple rovers simultaneously.


# 3. Change Requests

## CR-01 — Emergency Safety

### Original Requirement
FR-04:

The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

### Updated Requirement
FR-04:

The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

### Change
The requirement is now measurable because the response time is defined as 3 seconds and the emergency conditions are clearly specified.


## CR-02 — Mission Expansion

### Original Requirement
NFR-04:

The system should support communication with multiple rovers simultaneously.

### Updated Requirement
NFR-04:

The system shall support at least 20 simultaneously connected rovers.

### Change
The requirement is now measurable because the minimum number of simultaneously connected rovers is defined as 20.


## CR-03 — Security Upgrade

### Original Requirement
NFR-02:

Only authenticated Mission Control operators shall be permitted to issue rover commands.

### Updated Requirement
NFR-02:

The system shall require authenticated and role-authorized operators before accepting rover commands.

### Change
The security requirement now includes both authentication and role authorization.
