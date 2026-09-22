# Sprinkler-Bot
Autonomous mobile robot designed to identify plants, navigate between them and perform controlled watering.

<img width="839" height="696" alt="image" src="https://github.com/user-attachments/assets/35efcf3d-9c80-4fb2-b03a-4edffa544b19" />

The Sprinkler Bot is an autonomous mobile robot developed at
Polytech Nice Sophia for automated plant watering.

The robot combines:
- QR-code based plant identification
- Infrared line following
- Motor control
- Water pump control
- Water flow measurement
- A servo-driven watering mechanism

# Architecture 

                ┌─────────────────┐
                │   QR Scanner    │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Plant detection │
                └────────┬────────┘
                         │
                         ▼
    ┌─────────────┐   ┌───────────────┐   ┌──────────────┐
    │ IR sensors  │ → │ Arduino Mega  │ → │ Motor driver │
    └─────────────┘   └───────┬───────┘   └──────────────┘
                              ▼
                       ┌──────────────┐
                       │ Watering     │
                       │ system       │
                       └──────┬───────┘
                              │
                     ┌────────┴────────┐
                     │ Pump + flow     │
                     │ sensor + arm    │
                     └─────────────────┘
