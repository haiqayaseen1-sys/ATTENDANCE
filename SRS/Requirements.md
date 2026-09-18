
# Software Requirement Specification

## 1. Mission: Analyze the Engineering Note

### Functional Requirements

#### FR-01: Send Commands
Mission Control shall send movement commands to the rover.

#### FR-02: Execute Valid Commands
The rover shall receive and execute valid commands from Mission Control.

#### FR-03: Report Rover Status
The rover shall report its current position, battery level, temperature, and communication status.

#### FR-04: Safe Mode
The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

#### FR-05: Command Execution Status
Mission Control shall receive the status of command execution.

#### FR-06: Reject Invalid Commands
The system shall reject invalid or unauthorized commands.

#### FR-07: Record Mission Events
The system shall record all commands and critical rover events with a timestamp and operator ID.

#### FR-08: Detect Communication Failures
The system shall detect communication failures between Mission Control and the rover.

### Non-Functional Requirements

#### NFR-01: Performance
Command processing should normally complete within 5 seconds after a command is received by the rover.

#### NFR-02: Security
Only authenticated Mission Control operators shall be permitted to issue rover commands.

#### NFR-03: Reliability
The system shall continue operating despite temporary communication interruptions.

#### NFR-04: Scalability
The system should support communication with multiple rovers simultaneously.

## 2. Mission Control Sends Change Requests

### CR-01: Emergency Safety

**Original FR-04:**

The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

**New FR-04:**

The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

**Change:** The requirement is now measurable because it specifies a 3-second time limit and clear conditions for entering Safe Mode.


### CR-02: Mission Expansion

**Original NFR-04:**

The system shall support communication with multiple rovers simultaneously.

**New NFR-04:**

The system shall support at least 20 simultaneously connected rovers.

**Change:** The requirement is now measurable because it specifies support for at least 20 connected rovers.


### CR-03: Security Upgrade

**Original NFR-02:**

Only authenticated Mission Control operators shall be permitted to issue rover commands.

**New NFR-02:**

The system shall require authenticated and role-authorized operators before accepting rover commands.

**Change:** The security requirement is strengthened by requiring both authentication and role authorization before accepting commands.

