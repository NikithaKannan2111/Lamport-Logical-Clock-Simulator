# Lamport Logical Clock Simulator

A browser-based mini project for demonstrating Lamport logical clocks in a distributed system.

## Run the project
1. Download or clone this repository.
2. Open `index.html` in a modern web browser.
3. Add internal events, send messages, and receive queued messages.
4. Use **Reset simulation** to start again.

No installation, server, database, or external dependency is required.

## Features
- Three simulated processes: P1, P2, and P3
- Independent logical clocks
- Internal events
- Message sending with attached timestamps
- Message receiving using `max(local, received) + 1`
- Event log and per-process timeline
- Reset functionality

## Lamport clock rules
- Internal event: `C_i = C_i + 1`
- Send event: increment the sender clock and attach its value to the message
- Receive event: `C_j = max(C_j, T_m) + 1`

Here, `T_m` is the timestamp carried by the received message.

## Suggested demonstration
1. Add an internal event to P1.
2. Send a message from P1 to P2.
3. Receive the message at P2.
4. Observe that P2's clock becomes greater than both its previous clock and the message timestamp.
5. Repeat with P3 and compare event order.

## Repository structure
```text
lamport-logical-clock-project/
├── index.html
├── README.md
└── docs/
    ├── Mini_Project_Report.docx
    └── Mini_Project_Report.pdf
```

## Academic note
This is an educational simulation. It models logical-clock updates and message ordering; it is not a real networked distributed system.
