# FrankLaterza.github.io

This ESP32-based flight control training simulator prototype demonstrates hard real-time task scheduling for aerospace applications using FreeRTOS. The system implements five concurrent tasks including a hard real-time sensor sampling task (100ms period) that monitors a simulated G-sensor for hazard detection, and a hard real-time response task (10ms poll rate) that drives warning LED indicators when thresholds are exceeded. Inter-task communication is achieved through binary and counting semaphores for event queuing, plus a mutex to protect shared UART output, demonstrating multiple synchronization primitives working together. External communication is handled via a Wi-Fi web server that serves as an instructor console for toggling simulator panel annunciators, while an interrupt service routine provides deterministic pilot input handling for mode selection. The architecture prioritizes deterministic behavior and deadline guarantees, with all hard real-time tasks demonstrably meeting their timing constraints through heartbeat LED visualization and serial timestamp logging in the Wokwi simulation environment.

<iframe width="560" height="315" 
  src="https://www.youtube.com/embed/YG9saunQXLw" 
  frameborder="0" 
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
  allowfullscreen>
</iframe>
